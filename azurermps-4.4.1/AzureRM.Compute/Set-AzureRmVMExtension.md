---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
ms.openlocfilehash: da46aa0e6518c9a9eb9ebea58962f3da593ad264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430755"
---
# <span data-ttu-id="d8094-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="d8094-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="d8094-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8094-102">SYNOPSIS</span></span>
<span data-ttu-id="d8094-103">Atualiza as propriedades de extensão ou adiciona uma extensão a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8094-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8094-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8094-104">SYNTAX</span></span>

### <span data-ttu-id="d8094-105">Configurações (padrão)</span><span class="sxs-lookup"><span data-stu-id="d8094-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8094-106">Settingstring</span><span class="sxs-lookup"><span data-stu-id="d8094-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8094-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8094-107">DESCRIPTION</span></span>
<span data-ttu-id="d8094-108">O cmdlet **set-AzureRmVMExtension** atualiza as propriedades das extensões de máquina virtual existentes ou adiciona uma extensão a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8094-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="d8094-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8094-109">EXAMPLES</span></span>

### <span data-ttu-id="d8094-110">Exemplo 1: modificar as configurações usando tabelas de hash</span><span class="sxs-lookup"><span data-stu-id="d8094-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="d8094-111">Os primeiros dois comandos usam a sintaxe padrão do Windows PowerShell para criar tabelas de hash e, em seguida, armazenam essas tabelas de hash nas variáveis $Settings e $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="d8094-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="d8094-112">Para obter mais informações, digite `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="d8094-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="d8094-113">O segundo comando inclui dois valores criados anteriormente e armazenados em variáveis.</span><span class="sxs-lookup"><span data-stu-id="d8094-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="d8094-114">O comando final modifica uma extensão da máquina virtual nomeada VirtualMachine22 no ResourceGroup11 de acordo com o conteúdo de $Settings e $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="d8094-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="d8094-115">O comando especifica outras informações necessárias que incluem o fornecedor e o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="d8094-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="d8094-116">Exemplo 2: modificar as configurações usando cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="d8094-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="d8094-117">Os dois primeiros comandos criam cadeias de caracteres que contêm configurações e, em seguida, as armazena nas variáveis $SettingsString e $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="d8094-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="d8094-118">O comando final modifica uma extensão da máquina virtual nomeada VirtualMachine22 no ResourceGroup11 de acordo com o conteúdo de $SettingsString e $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="d8094-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="d8094-119">O comando especifica outras informações necessárias que incluem o fornecedor e o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="d8094-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="d8094-120">OS</span><span class="sxs-lookup"><span data-stu-id="d8094-120">PARAMETERS</span></span>

### <span data-ttu-id="d8094-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8094-121">-DefaultProfile</span></span>
<span data-ttu-id="d8094-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8094-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8094-123">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d8094-123">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d8094-124">Indica que esse cmdlet impede que o agente convidado do Azure atualize automaticamente as extensões para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="d8094-124">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="d8094-125">Por padrão, esse cmdlet permite que o agente de convidado atualize as extensões.</span><span class="sxs-lookup"><span data-stu-id="d8094-125">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="d8094-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="d8094-126">-ExtensionType</span></span>
<span data-ttu-id="d8094-127">Especifica o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="d8094-127">Specifies the extension type.</span></span>

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

### <span data-ttu-id="d8094-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="d8094-128">-ForceRerun</span></span>
<span data-ttu-id="d8094-129">Indica que esse cmdlet força uma nova configuração da mesma extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="d8094-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="d8094-130">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="d8094-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="d8094-131">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="d8094-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="d8094-132">-Local</span><span class="sxs-lookup"><span data-stu-id="d8094-132">-Location</span></span>
<span data-ttu-id="d8094-133">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8094-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="d8094-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8094-134">-Name</span></span>
<span data-ttu-id="d8094-135">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="d8094-135">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="d8094-136">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="d8094-136">-ProtectedSettings</span></span>
<span data-ttu-id="d8094-137">Especifica a configuração particular para a extensão, como uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d8094-137">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="d8094-138">Esse cmdlet criptografa a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="d8094-138">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="d8094-139">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="d8094-139">-ProtectedSettingString</span></span>
<span data-ttu-id="d8094-140">Especifica a configuração particular para a extensão, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d8094-140">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="d8094-141">Esse cmdlet criptografa a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="d8094-141">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="d8094-142">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d8094-142">-Publisher</span></span>
<span data-ttu-id="d8094-143">Especifica o nome do fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="d8094-143">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="d8094-144">O fornecedor fornece um nome quando o Publicador registra uma extensão.</span><span class="sxs-lookup"><span data-stu-id="d8094-144">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="d8094-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8094-145">-ResourceGroupName</span></span>
<span data-ttu-id="d8094-146">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8094-146">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d8094-147">-Configurações</span><span class="sxs-lookup"><span data-stu-id="d8094-147">-Settings</span></span>
<span data-ttu-id="d8094-148">Especifica a configuração pública para a extensão, como uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d8094-148">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="d8094-149">Este cmdlet não criptografa a configuração pública.</span><span class="sxs-lookup"><span data-stu-id="d8094-149">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="d8094-150">-Settingstring</span><span class="sxs-lookup"><span data-stu-id="d8094-150">-SettingString</span></span>
<span data-ttu-id="d8094-151">Especifica a configuração pública para a extensão, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d8094-151">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="d8094-152">Este cmdlet não criptografa a configuração pública.</span><span class="sxs-lookup"><span data-stu-id="d8094-152">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="d8094-153">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d8094-153">-TypeHandlerVersion</span></span>
<span data-ttu-id="d8094-154">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8094-154">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="d8094-155">-VMName</span><span class="sxs-lookup"><span data-stu-id="d8094-155">-VMName</span></span>
<span data-ttu-id="d8094-156">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8094-156">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d8094-157">Esse cmdlet modifica extensões para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d8094-157">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d8094-158">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d8094-158">-Confirm</span></span>
<span data-ttu-id="d8094-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8094-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8094-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8094-160">-WhatIf</span></span>
<span data-ttu-id="d8094-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8094-161">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d8094-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8094-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8094-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8094-163">CommonParameters</span></span>
<span data-ttu-id="d8094-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8094-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8094-165">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8094-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8094-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8094-166">INPUTS</span></span>

## <span data-ttu-id="d8094-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8094-167">OUTPUTS</span></span>

## <span data-ttu-id="d8094-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8094-168">NOTES</span></span>

## <span data-ttu-id="d8094-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8094-169">RELATED LINKS</span></span>

[<span data-ttu-id="d8094-170">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="d8094-170">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="d8094-171">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="d8094-171">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)


