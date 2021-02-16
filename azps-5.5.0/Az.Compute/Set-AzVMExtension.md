---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: dc19566a9baaee7aa70dc03e5d9effa22df8d758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117816"
---
# <span data-ttu-id="91871-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="91871-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="91871-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91871-102">SYNOPSIS</span></span>
<span data-ttu-id="91871-103">Atualiza as propriedades de extensão ou adiciona uma extensão a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91871-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="91871-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91871-104">SYNTAX</span></span>

### <span data-ttu-id="91871-105">Configurações (Padrão)</span><span class="sxs-lookup"><span data-stu-id="91871-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91871-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="91871-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91871-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="91871-107">DESCRIPTION</span></span>
<span data-ttu-id="91871-108">O cmdlet **Set-AzVMExtension** atualiza as propriedades das Extensões de Máquina Virtual existentes ou adiciona uma extensão a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91871-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="91871-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91871-109">EXAMPLES</span></span>

### <span data-ttu-id="91871-110">Exemplo 1: Modificar configurações usando tabelas hash</span><span class="sxs-lookup"><span data-stu-id="91871-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="91871-111">Os dois primeiros comandos usam a sintaxe padrão do Windows PowerShell para criar tabelas hash e, em seguida, armazena essas tabelas hash nas variáveis $Settings e $ProtectedSettings dados.</span><span class="sxs-lookup"><span data-stu-id="91871-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="91871-112">Para obter mais informações, digite `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="91871-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="91871-113">O segundo comando inclui dois valores criados anteriormente e armazenados em variáveis.</span><span class="sxs-lookup"><span data-stu-id="91871-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="91871-114">O comando final modifica uma extensão da máquina virtual chamada VirtualMachine22 no ResourceGroup11 de acordo com o conteúdo de $Settings e $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="91871-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="91871-115">O comando especifica outras informações necessárias que incluem o editor e o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="91871-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="91871-116">Exemplo 2: Modificar configurações usando cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="91871-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="91871-117">Os dois primeiros comandos criam cadeias de caracteres que contêm configurações e as armazena nas $SettingsString e $ProtectedSettingsString variáveis.</span><span class="sxs-lookup"><span data-stu-id="91871-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="91871-118">O comando final modifica uma extensão da máquina virtual chamada VirtualMachine22 no ResourceGroup11 de acordo com o conteúdo de $SettingsString e $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="91871-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="91871-119">O comando especifica outras informações necessárias que incluem o editor e o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="91871-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="91871-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91871-120">PARAMETERS</span></span>

### <span data-ttu-id="91871-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91871-121">-AsJob</span></span>
<span data-ttu-id="91871-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="91871-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91871-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91871-123">-DefaultProfile</span></span>
<span data-ttu-id="91871-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="91871-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91871-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="91871-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="91871-126">Indica que esse cmdlet impede que o agente convidado do Azure atualiza automaticamente as extensões para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="91871-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="91871-127">Por padrão, esse cmdlet permite que o agente convidado atualize as extensões.</span><span class="sxs-lookup"><span data-stu-id="91871-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="91871-128">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="91871-128">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="91871-129">Indica se a extensão deve ser atualizada automaticamente pela plataforma se houver uma versão mais recente da extensão disponível.</span><span class="sxs-lookup"><span data-stu-id="91871-129">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

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

### <span data-ttu-id="91871-130">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="91871-130">-ExtensionType</span></span>
<span data-ttu-id="91871-131">Especifica o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="91871-131">Specifies the extension type.</span></span>

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

### <span data-ttu-id="91871-132">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="91871-132">-ForceRerun</span></span>
<span data-ttu-id="91871-133">Indica que esse cmdlet força uma nova execução da mesma configuração de extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="91871-133">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="91871-134">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="91871-134">The value can be any string different from the current value.</span></span>
<span data-ttu-id="91871-135">Se forceUpdateTag não for alterado, as atualizações para configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="91871-135">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="91871-136">-Local</span><span class="sxs-lookup"><span data-stu-id="91871-136">-Location</span></span>
<span data-ttu-id="91871-137">Especifica a localização da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91871-137">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="91871-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="91871-138">-Name</span></span>
<span data-ttu-id="91871-139">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="91871-139">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="91871-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="91871-140">-NoWait</span></span>
<span data-ttu-id="91871-141">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="91871-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="91871-142">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="91871-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="91871-143">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="91871-143">-ProtectedSettings</span></span>
<span data-ttu-id="91871-144">Especifica a configuração privada para a extensão, como uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="91871-144">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="91871-145">Este cmdlet criptografa a configuração privada.</span><span class="sxs-lookup"><span data-stu-id="91871-145">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="91871-146">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="91871-146">-ProtectedSettingString</span></span>
<span data-ttu-id="91871-147">Especifica a configuração privada para a extensão, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="91871-147">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="91871-148">Este cmdlet criptografa a configuração privada.</span><span class="sxs-lookup"><span data-stu-id="91871-148">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="91871-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="91871-149">-Publisher</span></span>
<span data-ttu-id="91871-150">Especifica o nome do editor de extensão.</span><span class="sxs-lookup"><span data-stu-id="91871-150">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="91871-151">O editor fornece um nome quando o editor registra uma extensão.</span><span class="sxs-lookup"><span data-stu-id="91871-151">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="91871-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91871-152">-ResourceGroupName</span></span>
<span data-ttu-id="91871-153">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91871-153">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="91871-154">-Configurações</span><span class="sxs-lookup"><span data-stu-id="91871-154">-Settings</span></span>
<span data-ttu-id="91871-155">Especifica a configuração pública para a extensão, como uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="91871-155">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="91871-156">Este cmdlet não criptografa a configuração pública.</span><span class="sxs-lookup"><span data-stu-id="91871-156">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="91871-157">-SettingString</span><span class="sxs-lookup"><span data-stu-id="91871-157">-SettingString</span></span>
<span data-ttu-id="91871-158">Especifica a configuração pública para a extensão, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="91871-158">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="91871-159">Este cmdlet não criptografa a configuração pública.</span><span class="sxs-lookup"><span data-stu-id="91871-159">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="91871-160">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="91871-160">-TypeHandlerVersion</span></span>
<span data-ttu-id="91871-161">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91871-161">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="91871-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="91871-162">-VMName</span></span>
<span data-ttu-id="91871-163">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91871-163">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="91871-164">Este cmdlet modifica extensões para a máquina virtual especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="91871-164">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="91871-165">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="91871-165">-Confirm</span></span>
<span data-ttu-id="91871-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91871-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91871-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91871-167">-WhatIf</span></span>
<span data-ttu-id="91871-168">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="91871-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91871-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91871-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91871-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91871-170">CommonParameters</span></span>
<span data-ttu-id="91871-171">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91871-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91871-172">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91871-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91871-173">Entradas</span><span class="sxs-lookup"><span data-stu-id="91871-173">INPUTS</span></span>

### <span data-ttu-id="91871-174">System.String</span><span class="sxs-lookup"><span data-stu-id="91871-174">System.String</span></span>

### <span data-ttu-id="91871-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="91871-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="91871-176">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="91871-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="91871-177">Saídas</span><span class="sxs-lookup"><span data-stu-id="91871-177">OUTPUTS</span></span>

### <span data-ttu-id="91871-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="91871-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="91871-179">Notas</span><span class="sxs-lookup"><span data-stu-id="91871-179">NOTES</span></span>

## <span data-ttu-id="91871-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91871-180">RELATED LINKS</span></span>

[<span data-ttu-id="91871-181">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="91871-181">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="91871-182">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="91871-182">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


