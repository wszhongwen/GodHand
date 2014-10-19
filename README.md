函数用法：

一、施法类

1、castSpell(Unit,SpellID,FacingCheck,MovementCheck,SpamAllowed,KnownSkip)

参数：
UnitID 			对象
SpellID 		法术ID
Facing 			面向：设定为true则无视面向施法，设定为false则面对才施法
MovementCheck	移动状态：设定为true则站立时施法，设定为false则移动时也施法
SpamAllowed 	施法延迟：设定为true则忽略施法延迟，设定为false则施法此法术后1秒内不再释放此技能
KnownSkip 		是否学习此法术检测：设定为true忽略检测，设定为false则学习此法术才释放
实例：
    --毁灭打击
    if castSpell("target",20243,false,false) then
        return;
    end
	
    --震荡波
    if castSpell("target",46968,false,false,true,false) then
        return;
    end
