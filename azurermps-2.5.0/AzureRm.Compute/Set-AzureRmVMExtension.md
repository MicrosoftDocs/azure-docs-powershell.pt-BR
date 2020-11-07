---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmextension
schema: 2.0.0
ms.openlocfilehash: a714fb524de9c7c40c6b74dba321412e7aa457e6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786316"
---
# <span data-ttu-id="9d5b9-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="9d5b9-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="9d5b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d5b9-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5b9-103">Atualiza as propriedades de extensão ou adiciona uma extensão a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d5b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d5b9-104">SYNTAX</span></span>

### <span data-ttu-id="9d5b9-105">Configurações (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d5b9-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d5b9-106">Settingstring</span><span class="sxs-lookup"><span data-stu-id="9d5b9-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d5b9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d5b9-107">DESCRIPTION</span></span>
<span data-ttu-id="9d5b9-108">O cmdlet **set-AzureRmVMExtension** atualiza as propriedades das extensões de máquina virtual existentes ou adiciona uma extensão a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="9d5b9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d5b9-109">EXAMPLES</span></span>

### <span data-ttu-id="9d5b9-110">Exemplo 1: modificar as configurações usando tabelas de hash</span><span class="sxs-lookup"><span data-stu-id="9d5b9-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="9d5b9-111">Os primeiros dois comandos usam a sintaxe padrão do Windows PowerShell para criar tabelas de hash e, em seguida, armazenam essas tabelas de hash nas variáveis $Settings e $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="9d5b9-112">Para obter mais informações, digite `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="9d5b9-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="9d5b9-113">O segundo comando inclui dois valores criados anteriormente e armazenados em variáveis.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="9d5b9-114">O comando final modifica uma extensão da máquina virtual nomeada VirtualMachine22 no ResourceGroup11 de acordo com o conteúdo de $Settings e $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="9d5b9-115">O comando especifica outras informações necessárias que incluem o fornecedor e o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="9d5b9-116">Exemplo 2: modificar as configurações usando cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="9d5b9-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="9d5b9-117">Os dois primeiros comandos criam cadeias de caracteres que contêm configurações e, em seguida, as armazena nas variáveis $SettingsString e $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="9d5b9-118">O comando final modifica uma extensão da máquina virtual nomeada VirtualMachine22 no ResourceGroup11 de acordo com o conteúdo de $SettingsString e $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="9d5b9-119">O comando especifica outras informações necessárias que incluem o fornecedor e o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="9d5b9-120">OS</span><span class="sxs-lookup"><span data-stu-id="9d5b9-120">PARAMETERS</span></span>

### <span data-ttu-id="9d5b9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d5b9-121">-AsJob</span></span>
<span data-ttu-id="9d5b9-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9d5b9-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d5b9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d5b9-123">-DefaultProfile</span></span>
<span data-ttu-id="9d5b9-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d5b9-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="9d5b9-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="9d5b9-126">Indica que esse cmdlet impede que o agente convidado do Azure atualize automaticamente as extensões para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="9d5b9-127">Por padrão, esse cmdlet permite que o agente de convidado atualize as extensões.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="9d5b9-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="9d5b9-128">-ExtensionType</span></span>
<span data-ttu-id="9d5b9-129">Especifica o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-129">Specifies the extension type.</span></span>

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

### <span data-ttu-id="9d5b9-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="9d5b9-130">-ForceRerun</span></span>
<span data-ttu-id="9d5b9-131">Indica que esse cmdlet força uma nova configuração da mesma extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="9d5b9-132">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-132">The value can be any string different from the current value.</span></span>

<span data-ttu-id="9d5b9-133">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="9d5b9-134">-Local</span><span class="sxs-lookup"><span data-stu-id="9d5b9-134">-Location</span></span>
<span data-ttu-id="9d5b9-135">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-135">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="9d5b9-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d5b9-136">-Name</span></span>
<span data-ttu-id="9d5b9-137">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-137">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="9d5b9-138">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="9d5b9-138">-ProtectedSettings</span></span>
<span data-ttu-id="9d5b9-139">Especifica a configuração particular para a extensão, como uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-139">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="9d5b9-140">Esse cmdlet criptografa a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-140">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="9d5b9-141">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="9d5b9-141">-ProtectedSettingString</span></span>
<span data-ttu-id="9d5b9-142">Especifica a configuração particular para a extensão, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-142">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="9d5b9-143">Esse cmdlet criptografa a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-143">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="9d5b9-144">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9d5b9-144">-Publisher</span></span>
<span data-ttu-id="9d5b9-145">Especifica o nome do fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-145">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="9d5b9-146">O fornecedor fornece um nome quando o Publicador registra uma extensão.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-146">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="9d5b9-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d5b9-147">-ResourceGroupName</span></span>
<span data-ttu-id="9d5b9-148">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-148">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9d5b9-149">-Configurações</span><span class="sxs-lookup"><span data-stu-id="9d5b9-149">-Settings</span></span>
<span data-ttu-id="9d5b9-150">Especifica a configuração pública para a extensão, como uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-150">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="9d5b9-151">Este cmdlet não criptografa a configuração pública.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-151">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="9d5b9-152">-Settingstring</span><span class="sxs-lookup"><span data-stu-id="9d5b9-152">-SettingString</span></span>
<span data-ttu-id="9d5b9-153">Especifica a configuração pública para a extensão, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-153">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="9d5b9-154">Este cmdlet não criptografa a configuração pública.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-154">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="9d5b9-155">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="9d5b9-155">-TypeHandlerVersion</span></span>
<span data-ttu-id="9d5b9-156">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-156">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="9d5b9-157">-VMName</span><span class="sxs-lookup"><span data-stu-id="9d5b9-157">-VMName</span></span>
<span data-ttu-id="9d5b9-158">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-158">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9d5b9-159">Esse cmdlet modifica extensões para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-159">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="9d5b9-160">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9d5b9-160">-Confirm</span></span>
<span data-ttu-id="9d5b9-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d5b9-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d5b9-162">-WhatIf</span></span>
<span data-ttu-id="9d5b9-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-163">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9d5b9-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d5b9-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d5b9-165">CommonParameters</span></span>
<span data-ttu-id="9d5b9-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d5b9-167">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d5b9-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d5b9-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d5b9-168">INPUTS</span></span>

### <span data-ttu-id="9d5b9-169">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9d5b9-169">None</span></span>
<span data-ttu-id="9d5b9-170">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="9d5b9-170">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d5b9-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d5b9-171">OUTPUTS</span></span>

### <span data-ttu-id="9d5b9-172">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9d5b9-172">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9d5b9-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d5b9-173">NOTES</span></span>

## <span data-ttu-id="9d5b9-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d5b9-174">RELATED LINKS</span></span>

[<span data-ttu-id="9d5b9-175">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="9d5b9-175">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="9d5b9-176">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="9d5b9-176">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)


