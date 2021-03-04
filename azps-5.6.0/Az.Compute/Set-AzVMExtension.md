---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: b1c7a45f538c10c2ef6c2f03809a127a21237fc9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888993"
---
# <span data-ttu-id="5a224-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="5a224-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="5a224-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a224-102">SYNOPSIS</span></span>
<span data-ttu-id="5a224-103">Atualiza propriedades de extensão ou adiciona uma extensão a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a224-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="5a224-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5a224-104">SYNTAX</span></span>

### <span data-ttu-id="5a224-105">Configurações (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5a224-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a224-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="5a224-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a224-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5a224-107">DESCRIPTION</span></span>
<span data-ttu-id="5a224-108">O cmdlet **Set-AzVMExtension** atualiza propriedades para extensões de máquina virtual existentes ou adiciona uma extensão a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a224-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="5a224-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a224-109">EXAMPLES</span></span>

### <span data-ttu-id="5a224-110">Exemplo 1: Modificar configurações usando tabelas de hash</span><span class="sxs-lookup"><span data-stu-id="5a224-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="5a224-111">Os dois primeiros comandos usam a sintaxe Windows PowerShell padrão para criar tabelas de hash e, em seguida, armazenam essas tabelas de hash nas $Settings e $ProtectedSettings variáveis.</span><span class="sxs-lookup"><span data-stu-id="5a224-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="5a224-112">Para obter mais informações, digite `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="5a224-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="5a224-113">O segundo comando inclui dois valores criados anteriormente e armazenados em variáveis.</span><span class="sxs-lookup"><span data-stu-id="5a224-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="5a224-114">O comando final modifica uma extensão da máquina virtual chamada VirtualMachine22 em ResourceGroup11 de acordo com o conteúdo de $Settings e $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="5a224-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="5a224-115">O comando especifica outras informações necessárias que incluem o editor e o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="5a224-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="5a224-116">Exemplo 2: Modificar configurações usando cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="5a224-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="5a224-117">Os dois primeiros comandos criam cadeias de caracteres que contêm configurações e as armazenam nas $SettingsString e $ProtectedSettingsString variáveis.</span><span class="sxs-lookup"><span data-stu-id="5a224-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="5a224-118">O comando final modifica uma extensão da máquina virtual chamada VirtualMachine22 em ResourceGroup11 de acordo com o conteúdo de $SettingsString e $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="5a224-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="5a224-119">O comando especifica outras informações necessárias que incluem o editor e o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="5a224-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="5a224-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5a224-120">PARAMETERS</span></span>

### <span data-ttu-id="5a224-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a224-121">-AsJob</span></span>
<span data-ttu-id="5a224-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5a224-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a224-123">-DefaultProfile</span></span>
<span data-ttu-id="5a224-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5a224-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5a224-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="5a224-126">Indica que esse cmdlet impede que o agente convidado do Azure atualiza automaticamente as extensões para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="5a224-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="5a224-127">Por padrão, esse cmdlet permite que o agente convidado atualize as extensões.</span><span class="sxs-lookup"><span data-stu-id="5a224-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-128">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="5a224-128">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="5a224-129">Indica se a extensão deve ser atualizada automaticamente pela plataforma se houver uma versão mais recente da extensão disponível.</span><span class="sxs-lookup"><span data-stu-id="5a224-129">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-130">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="5a224-130">-ExtensionType</span></span>
<span data-ttu-id="5a224-131">Especifica o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="5a224-131">Specifies the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-132">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="5a224-132">-ForceRerun</span></span>
<span data-ttu-id="5a224-133">Indica que esse cmdlet força uma repetição da mesma configuração de extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="5a224-133">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="5a224-134">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="5a224-134">The value can be any string different from the current value.</span></span>
<span data-ttu-id="5a224-135">Se forceUpdateTag não for alterado, as atualizações para configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="5a224-135">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-136">-Location</span><span class="sxs-lookup"><span data-stu-id="5a224-136">-Location</span></span>
<span data-ttu-id="5a224-137">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a224-137">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-138">-Name</span><span class="sxs-lookup"><span data-stu-id="5a224-138">-Name</span></span>
<span data-ttu-id="5a224-139">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="5a224-139">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5a224-140">-NoWait</span></span>
<span data-ttu-id="5a224-141">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="5a224-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="5a224-142">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="5a224-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-143">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="5a224-143">-ProtectedSettings</span></span>
<span data-ttu-id="5a224-144">Especifica a configuração privada para a extensão, como uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5a224-144">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="5a224-145">Este cmdlet criptografa a configuração privada.</span><span class="sxs-lookup"><span data-stu-id="5a224-145">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-146">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="5a224-146">-ProtectedSettingString</span></span>
<span data-ttu-id="5a224-147">Especifica a configuração privada para a extensão, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5a224-147">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="5a224-148">Este cmdlet criptografa a configuração privada.</span><span class="sxs-lookup"><span data-stu-id="5a224-148">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="5a224-149">-Publisher</span></span>
<span data-ttu-id="5a224-150">Especifica o nome do editor de extensão.</span><span class="sxs-lookup"><span data-stu-id="5a224-150">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="5a224-151">O editor fornece um nome quando o editor registra uma extensão.</span><span class="sxs-lookup"><span data-stu-id="5a224-151">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a224-152">-ResourceGroupName</span></span>
<span data-ttu-id="5a224-153">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a224-153">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-154">-Settings</span><span class="sxs-lookup"><span data-stu-id="5a224-154">-Settings</span></span>
<span data-ttu-id="5a224-155">Especifica a configuração pública para a extensão, como uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5a224-155">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="5a224-156">Este cmdlet não criptografa a configuração pública.</span><span class="sxs-lookup"><span data-stu-id="5a224-156">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-157">-SettingString</span><span class="sxs-lookup"><span data-stu-id="5a224-157">-SettingString</span></span>
<span data-ttu-id="5a224-158">Especifica a configuração pública para a extensão, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5a224-158">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="5a224-159">Este cmdlet não criptografa a configuração pública.</span><span class="sxs-lookup"><span data-stu-id="5a224-159">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-160">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5a224-160">-TypeHandlerVersion</span></span>
<span data-ttu-id="5a224-161">Especifica a versão da extensão a ser usada para essa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a224-161">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="5a224-162">-VMName</span></span>
<span data-ttu-id="5a224-163">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a224-163">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5a224-164">Este cmdlet modifica extensões para a máquina virtual especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5a224-164">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a224-165">-Confirm</span></span>
<span data-ttu-id="5a224-166">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a224-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a224-167">-WhatIf</span></span>
<span data-ttu-id="5a224-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5a224-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a224-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a224-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a224-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a224-170">CommonParameters</span></span>
<span data-ttu-id="5a224-171">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a224-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a224-172">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a224-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a224-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a224-173">INPUTS</span></span>

### <span data-ttu-id="5a224-174">System.String</span><span class="sxs-lookup"><span data-stu-id="5a224-174">System.String</span></span>

### <span data-ttu-id="5a224-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5a224-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5a224-176">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5a224-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5a224-177">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5a224-177">OUTPUTS</span></span>

### <span data-ttu-id="5a224-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5a224-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5a224-179">NOTES</span><span class="sxs-lookup"><span data-stu-id="5a224-179">NOTES</span></span>

## <span data-ttu-id="5a224-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a224-180">RELATED LINKS</span></span>

[<span data-ttu-id="5a224-181">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="5a224-181">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="5a224-182">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="5a224-182">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


