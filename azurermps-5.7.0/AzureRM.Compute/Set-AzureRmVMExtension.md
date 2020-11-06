---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
ms.openlocfilehash: 1f758f77fc7162f8110f0e2d5887eadb55d7f7c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602030"
---
# <span data-ttu-id="db27a-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="db27a-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="db27a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db27a-102">SYNOPSIS</span></span>
<span data-ttu-id="db27a-103">Atualiza as propriedades de extensão ou adiciona uma extensão a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="db27a-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db27a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db27a-104">SYNTAX</span></span>

### <span data-ttu-id="db27a-105">Configurações (padrão)</span><span class="sxs-lookup"><span data-stu-id="db27a-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db27a-106">Settingstring</span><span class="sxs-lookup"><span data-stu-id="db27a-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db27a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db27a-107">DESCRIPTION</span></span>
<span data-ttu-id="db27a-108">O cmdlet **set-AzureRmVMExtension** atualiza as propriedades das extensões de máquina virtual existentes ou adiciona uma extensão a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="db27a-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="db27a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db27a-109">EXAMPLES</span></span>

### <span data-ttu-id="db27a-110">Exemplo 1: modificar as configurações usando tabelas de hash</span><span class="sxs-lookup"><span data-stu-id="db27a-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="db27a-111">Os primeiros dois comandos usam a sintaxe padrão do Windows PowerShell para criar tabelas de hash e, em seguida, armazenam essas tabelas de hash nas variáveis $Settings e $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="db27a-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="db27a-112">Para obter mais informações, digite `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="db27a-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="db27a-113">O segundo comando inclui dois valores criados anteriormente e armazenados em variáveis.</span><span class="sxs-lookup"><span data-stu-id="db27a-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="db27a-114">O comando final modifica uma extensão da máquina virtual nomeada VirtualMachine22 no ResourceGroup11 de acordo com o conteúdo de $Settings e $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="db27a-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="db27a-115">O comando especifica outras informações necessárias que incluem o fornecedor e o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="db27a-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="db27a-116">Exemplo 2: modificar as configurações usando cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="db27a-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="db27a-117">Os dois primeiros comandos criam cadeias de caracteres que contêm configurações e, em seguida, as armazena nas variáveis $SettingsString e $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="db27a-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="db27a-118">O comando final modifica uma extensão da máquina virtual nomeada VirtualMachine22 no ResourceGroup11 de acordo com o conteúdo de $SettingsString e $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="db27a-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="db27a-119">O comando especifica outras informações necessárias que incluem o fornecedor e o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="db27a-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="db27a-120">OS</span><span class="sxs-lookup"><span data-stu-id="db27a-120">PARAMETERS</span></span>

### <span data-ttu-id="db27a-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="db27a-121">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="db27a-122">Indica que esse cmdlet impede que o agente convidado do Azure atualize automaticamente as extensões para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="db27a-122">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="db27a-123">Por padrão, esse cmdlet permite que o agente de convidado atualize as extensões.</span><span class="sxs-lookup"><span data-stu-id="db27a-123">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db27a-124">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="db27a-124">-ExtensionType</span></span>
<span data-ttu-id="db27a-125">Especifica o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="db27a-125">Specifies the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db27a-126">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="db27a-126">-ForceRerun</span></span>
<span data-ttu-id="db27a-127">Indica que esse cmdlet força uma nova configuração da mesma extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="db27a-127">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="db27a-128">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="db27a-128">The value can be any string different from the current value.</span></span>

<span data-ttu-id="db27a-129">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="db27a-129">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db27a-130">-Local</span><span class="sxs-lookup"><span data-stu-id="db27a-130">-Location</span></span>
<span data-ttu-id="db27a-131">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="db27a-131">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db27a-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="db27a-132">-Name</span></span>
<span data-ttu-id="db27a-133">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="db27a-133">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db27a-134">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="db27a-134">-ProtectedSettings</span></span>
<span data-ttu-id="db27a-135">Especifica a configuração particular para a extensão, como uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="db27a-135">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="db27a-136">Esse cmdlet criptografa a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="db27a-136">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db27a-137">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="db27a-137">-ProtectedSettingString</span></span>
<span data-ttu-id="db27a-138">Especifica a configuração particular para a extensão, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="db27a-138">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="db27a-139">Esse cmdlet criptografa a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="db27a-139">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db27a-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="db27a-140">-Publisher</span></span>
<span data-ttu-id="db27a-141">Especifica o nome do fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="db27a-141">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="db27a-142">O fornecedor fornece um nome quando o Publicador registra uma extensão.</span><span class="sxs-lookup"><span data-stu-id="db27a-142">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db27a-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db27a-143">-ResourceGroupName</span></span>
<span data-ttu-id="db27a-144">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="db27a-144">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db27a-145">-Configurações</span><span class="sxs-lookup"><span data-stu-id="db27a-145">-Settings</span></span>
<span data-ttu-id="db27a-146">Especifica a configuração pública para a extensão, como uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="db27a-146">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="db27a-147">Este cmdlet não criptografa a configuração pública.</span><span class="sxs-lookup"><span data-stu-id="db27a-147">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db27a-148">-Settingstring</span><span class="sxs-lookup"><span data-stu-id="db27a-148">-SettingString</span></span>
<span data-ttu-id="db27a-149">Especifica a configuração pública para a extensão, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="db27a-149">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="db27a-150">Este cmdlet não criptografa a configuração pública.</span><span class="sxs-lookup"><span data-stu-id="db27a-150">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db27a-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="db27a-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="db27a-152">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="db27a-152">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db27a-153">-VMName</span><span class="sxs-lookup"><span data-stu-id="db27a-153">-VMName</span></span>
<span data-ttu-id="db27a-154">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="db27a-154">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="db27a-155">Esse cmdlet modifica extensões para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="db27a-155">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db27a-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="db27a-156">-Confirm</span></span>
<span data-ttu-id="db27a-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db27a-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db27a-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db27a-158">-WhatIf</span></span>
<span data-ttu-id="db27a-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db27a-159">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="db27a-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db27a-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db27a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db27a-161">CommonParameters</span></span>
<span data-ttu-id="db27a-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db27a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db27a-163">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db27a-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db27a-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db27a-164">INPUTS</span></span>

### <span data-ttu-id="db27a-165">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="db27a-165">None</span></span>
<span data-ttu-id="db27a-166">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="db27a-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db27a-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db27a-167">OUTPUTS</span></span>

## <span data-ttu-id="db27a-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db27a-168">NOTES</span></span>

## <span data-ttu-id="db27a-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db27a-169">RELATED LINKS</span></span>

[<span data-ttu-id="db27a-170">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="db27a-170">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="db27a-171">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="db27a-171">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)


