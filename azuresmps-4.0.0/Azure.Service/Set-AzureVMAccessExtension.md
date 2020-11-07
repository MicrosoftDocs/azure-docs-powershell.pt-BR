---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8F881112-3603-4EE7-88A4-ED45040A60AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc71708c0dff8e359813bb01db0f09f2c91a0cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945811"
---
# <span data-ttu-id="771a2-101">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="771a2-101">Set-AzureVMAccessExtension</span></span>

## <span data-ttu-id="771a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="771a2-102">SYNOPSIS</span></span>
<span data-ttu-id="771a2-103">Define a extensão VMAccess para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="771a2-103">Sets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="771a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="771a2-104">SYNTAX</span></span>

### <span data-ttu-id="771a2-105">EnableAccessExtension (padrão)</span><span class="sxs-lookup"><span data-stu-id="771a2-105">EnableAccessExtension (Default)</span></span>
```
Set-AzureVMAccessExtension [[-UserName] <String>] [[-Password] <String>] [[-ReferenceName] <String>]
 [[-Version] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="771a2-106">DisableAccessExtension</span><span class="sxs-lookup"><span data-stu-id="771a2-106">DisableAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="771a2-107">UninstallAccessExtension</span><span class="sxs-lookup"><span data-stu-id="771a2-107">UninstallAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="771a2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="771a2-108">DESCRIPTION</span></span>
<span data-ttu-id="771a2-109">O cmdlet **set-AzureVMAccessExtension** adiciona a extensão VMAccess da máquina virtual a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="771a2-109">The **Set-AzureVMAccessExtension** cmdlet adds the Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="771a2-110">A extensão VMAccess pode ser usada para definir uma senha temporária e deve ser imediatamente alterada após o login na máquina.</span><span class="sxs-lookup"><span data-stu-id="771a2-110">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="771a2-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="771a2-111">EXAMPLES</span></span>

### <span data-ttu-id="771a2-112">Exemplo 1: definir a extensão VMAccess aplicada a uma máquina virtual especificada</span><span class="sxs-lookup"><span data-stu-id="771a2-112">Example 1: Set the VMAccess extension applied to a specified virtual machine</span></span>
```
PS C:\> Set-AzureVMAccessExtension -VM $VM -UserName $User -Password $PWD;
```

<span data-ttu-id="771a2-113">Esse comando define a extensão VMAccess aplicada à máquina virtual especificada, conforme armazenada na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="771a2-113">This command sets the VMAccess extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="771a2-114">OS</span><span class="sxs-lookup"><span data-stu-id="771a2-114">PARAMETERS</span></span>

### <span data-ttu-id="771a2-115">-Disable</span><span class="sxs-lookup"><span data-stu-id="771a2-115">-Disable</span></span>
<span data-ttu-id="771a2-116">Indica que esse cmdlet define o estado da extensão como Disable.</span><span class="sxs-lookup"><span data-stu-id="771a2-116">Indicates that this cmdlet sets the Extension State to Disable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771a2-117">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="771a2-117">-ForceUpdate</span></span>
<span data-ttu-id="771a2-118">Indica que esse cmdlet reaplica uma configuração a uma extensão quando a configuração não foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="771a2-118">Indicates that this cmdlet reapplies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="771a2-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="771a2-119">-InformationAction</span></span>
<span data-ttu-id="771a2-120">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="771a2-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="771a2-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="771a2-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="771a2-122">Contínuo</span><span class="sxs-lookup"><span data-stu-id="771a2-122">Continue</span></span>
- <span data-ttu-id="771a2-123">Ignorar</span><span class="sxs-lookup"><span data-stu-id="771a2-123">Ignore</span></span>
- <span data-ttu-id="771a2-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="771a2-124">Inquire</span></span>
- <span data-ttu-id="771a2-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="771a2-125">SilentlyContinue</span></span>
- <span data-ttu-id="771a2-126">Finaliza</span><span class="sxs-lookup"><span data-stu-id="771a2-126">Stop</span></span>
- <span data-ttu-id="771a2-127">Suspensão</span><span class="sxs-lookup"><span data-stu-id="771a2-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="771a2-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="771a2-128">-InformationVariable</span></span>
<span data-ttu-id="771a2-129">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="771a2-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="771a2-130">-Senha</span><span class="sxs-lookup"><span data-stu-id="771a2-130">-Password</span></span>
<span data-ttu-id="771a2-131">Especifica a senha para redefinir a credencial da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="771a2-131">Specifies the password for resetting the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771a2-132">-Perfil</span><span class="sxs-lookup"><span data-stu-id="771a2-132">-Profile</span></span>
<span data-ttu-id="771a2-133">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="771a2-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="771a2-134">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="771a2-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="771a2-135">-Referencename</span><span class="sxs-lookup"><span data-stu-id="771a2-135">-ReferenceName</span></span>
<span data-ttu-id="771a2-136">Especifica o nome de referência da extensão de acesso.</span><span class="sxs-lookup"><span data-stu-id="771a2-136">Specifies the reference name of the access extension.</span></span>

<span data-ttu-id="771a2-137">Esta é uma cadeia de caracteres definida pelo usuário que é usada para fazer referência a uma extensão.</span><span class="sxs-lookup"><span data-stu-id="771a2-137">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="771a2-138">Ele é especificado quando a extensão é adicionada à máquina virtual pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="771a2-138">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="771a2-139">Para atualizações subsequentes, você deve especificar o nome de referência usado anteriormente ao atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="771a2-139">For subsequent updates, you should specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="771a2-140">O *referencename* atribuído a uma extensão é retornado usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="771a2-140">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771a2-141">-Desinstalar</span><span class="sxs-lookup"><span data-stu-id="771a2-141">-Uninstall</span></span>
<span data-ttu-id="771a2-142">Indica se esse cmdlet desinstala a extensão de acesso.</span><span class="sxs-lookup"><span data-stu-id="771a2-142">Indicates whether this cmdlet uninstalls the access extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771a2-143">-UserName</span><span class="sxs-lookup"><span data-stu-id="771a2-143">-UserName</span></span>
<span data-ttu-id="771a2-144">Especifica o nome de usuário que este cmdlet usa para redefinir a credencial da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="771a2-144">Specifies the user name that this cmdlet uses to reset the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771a2-145">-Versão</span><span class="sxs-lookup"><span data-stu-id="771a2-145">-Version</span></span>
<span data-ttu-id="771a2-146">Especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="771a2-146">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771a2-147">-VM</span><span class="sxs-lookup"><span data-stu-id="771a2-147">-VM</span></span>
<span data-ttu-id="771a2-148">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="771a2-148">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="771a2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="771a2-149">CommonParameters</span></span>
<span data-ttu-id="771a2-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="771a2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="771a2-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="771a2-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="771a2-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="771a2-152">INPUTS</span></span>

## <span data-ttu-id="771a2-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="771a2-153">OUTPUTS</span></span>

## <span data-ttu-id="771a2-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="771a2-154">NOTES</span></span>

## <span data-ttu-id="771a2-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="771a2-155">RELATED LINKS</span></span>

[<span data-ttu-id="771a2-156">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="771a2-156">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="771a2-157">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="771a2-157">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)


