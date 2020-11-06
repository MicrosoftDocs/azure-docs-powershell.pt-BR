---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: a9d03bd7f506c7210eeee90c379f90dd0833818e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426930"
---
# <span data-ttu-id="51316-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="51316-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="51316-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51316-102">SYNOPSIS</span></span>
<span data-ttu-id="51316-103">Adiciona uma extensão de script personalizada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="51316-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51316-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51316-104">SYNTAX</span></span>

### <span data-ttu-id="51316-105">SetCustomScriptExtensionByContainerAndFileNames (padrão)</span><span class="sxs-lookup"><span data-stu-id="51316-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51316-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="51316-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51316-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51316-107">DESCRIPTION</span></span>
<span data-ttu-id="51316-108">O cmdlet **set-AzureRmVMCustomScriptExtension** adiciona uma extensão de máquina virtual de script personalizado a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="51316-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="51316-109">Essa extensão permite que você execute seus próprios scripts na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="51316-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="51316-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51316-110">EXAMPLES</span></span>

### <span data-ttu-id="51316-111">Exemplo 1: adicionar um script personalizado</span><span class="sxs-lookup"><span data-stu-id="51316-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="51316-112">Esse comando adiciona um script personalizado à máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="51316-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="51316-113">O arquivo de script é contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="51316-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="51316-114">OS</span><span class="sxs-lookup"><span data-stu-id="51316-114">PARAMETERS</span></span>

### <span data-ttu-id="51316-115">-Argumento</span><span class="sxs-lookup"><span data-stu-id="51316-115">-Argument</span></span>
<span data-ttu-id="51316-116">Especifica os argumentos que a extensão de script passa para o script.</span><span class="sxs-lookup"><span data-stu-id="51316-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="51316-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="51316-117">-ContainerName</span></span>
<span data-ttu-id="51316-118">Especifica o nome do contêiner de armazenamento do Azure em que esse cmdlet armazena o script.</span><span class="sxs-lookup"><span data-stu-id="51316-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51316-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51316-119">-DefaultProfile</span></span>
<span data-ttu-id="51316-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51316-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51316-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="51316-121">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="51316-122">-Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="51316-122">-FileName</span></span>
<span data-ttu-id="51316-123">Especifica o nome do arquivo de script.</span><span class="sxs-lookup"><span data-stu-id="51316-123">Specifies the name of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51316-124">-FileUri</span><span class="sxs-lookup"><span data-stu-id="51316-124">-FileUri</span></span>
<span data-ttu-id="51316-125">Especifica o URI do arquivo de script.</span><span class="sxs-lookup"><span data-stu-id="51316-125">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51316-126">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="51316-126">-ForceRerun</span></span>
<span data-ttu-id="51316-127">Indica que esse cmdlet força uma nova configuração da mesma extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="51316-127">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="51316-128">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="51316-128">The value can be any string different from the current value.</span></span>

<span data-ttu-id="51316-129">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="51316-129">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="51316-130">-Local</span><span class="sxs-lookup"><span data-stu-id="51316-130">-Location</span></span>
<span data-ttu-id="51316-131">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="51316-131">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="51316-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="51316-132">-Name</span></span>
<span data-ttu-id="51316-133">Especifica o nome da extensão de script personalizada.</span><span class="sxs-lookup"><span data-stu-id="51316-133">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="51316-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51316-134">-ResourceGroupName</span></span>
<span data-ttu-id="51316-135">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="51316-135">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="51316-136">-Executar</span><span class="sxs-lookup"><span data-stu-id="51316-136">-Run</span></span>
<span data-ttu-id="51316-137">Especifica o comando a ser usado para executar o script.</span><span class="sxs-lookup"><span data-stu-id="51316-137">Specifies the command to use that runs your script.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51316-138">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="51316-138">-SecureExecution</span></span>
<span data-ttu-id="51316-139">Indica que esse cmdlet garante que o valor do parâmetro de *execução* não esteja conectado ao servidor ou retornado ao usuário usando a API de extensão Get.</span><span class="sxs-lookup"><span data-stu-id="51316-139">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="51316-140">O valor de *Run* pode conter segredos ou senhas a serem passados para o arquivo de script com segurança.</span><span class="sxs-lookup"><span data-stu-id="51316-140">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="51316-141">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="51316-141">-StorageAccountKey</span></span>
<span data-ttu-id="51316-142">Especifica a chave para o contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="51316-142">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51316-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="51316-143">-StorageAccountName</span></span>
<span data-ttu-id="51316-144">Especifica o nome da conta de armazenamento do Azure na qual esse cmdlet armazena o script.</span><span class="sxs-lookup"><span data-stu-id="51316-144">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51316-145">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="51316-145">-StorageEndpointSuffix</span></span>
<span data-ttu-id="51316-146">Especifica o sufixo de ponto de extremidade de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="51316-146">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51316-147">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="51316-147">-TypeHandlerVersion</span></span>
<span data-ttu-id="51316-148">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="51316-148">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="51316-149">Para obter a versão, execute o cmdlet Get-AzureRmVMExtensionImage com um valor de Microsoft. COMPUTE para o parâmetro *PublisherName* e VMAccessAgent para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="51316-149">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="51316-150">-VMName</span><span class="sxs-lookup"><span data-stu-id="51316-150">-VMName</span></span>
<span data-ttu-id="51316-151">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="51316-151">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="51316-152">Esse cmdlet adiciona a extensão de script personalizada para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="51316-152">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="51316-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="51316-153">-Confirm</span></span>
<span data-ttu-id="51316-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51316-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51316-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51316-155">-WhatIf</span></span>
<span data-ttu-id="51316-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51316-156">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="51316-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51316-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51316-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51316-158">CommonParameters</span></span>
<span data-ttu-id="51316-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51316-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51316-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51316-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51316-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51316-161">INPUTS</span></span>

## <span data-ttu-id="51316-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51316-162">OUTPUTS</span></span>

## <span data-ttu-id="51316-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51316-163">NOTES</span></span>

## <span data-ttu-id="51316-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51316-164">RELATED LINKS</span></span>

[<span data-ttu-id="51316-165">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="51316-165">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="51316-166">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="51316-166">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)


