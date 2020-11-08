---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: baff896564d8f3b8d70f69b190bc3429d4f465c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125741"
---
# <span data-ttu-id="8dee6-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="8dee6-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="8dee6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8dee6-102">SYNOPSIS</span></span>
<span data-ttu-id="8dee6-103">Adicionar extensão de VM ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="8dee6-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="8dee6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8dee6-104">SYNTAX</span></span>

### <span data-ttu-id="8dee6-105">ByObj (padrão)</span><span class="sxs-lookup"><span data-stu-id="8dee6-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8dee6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8dee6-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8dee6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8dee6-107">DESCRIPTION</span></span>
<span data-ttu-id="8dee6-108">Adicionar extensão de VM ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="8dee6-108">Add vm extension to the node type.</span></span> <span data-ttu-id="8dee6-109">Isso adicionará a extensão ao recurso do conjunto de escala da máquina virtual underliying.</span><span class="sxs-lookup"><span data-stu-id="8dee6-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="8dee6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8dee6-110">EXAMPLES</span></span>

### <span data-ttu-id="8dee6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8dee6-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="8dee6-112">Esse comando adiciona uma extensão ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="8dee6-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="8dee6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8dee6-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="8dee6-114">Esse comando adiciona uma extensão com configurações e configurações protegidas ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="8dee6-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="8dee6-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8dee6-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="8dee6-116">Esse comando adiciona uma extensão ao tipo de nó, com tubulação.</span><span class="sxs-lookup"><span data-stu-id="8dee6-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="8dee6-117">OS</span><span class="sxs-lookup"><span data-stu-id="8dee6-117">PARAMETERS</span></span>

### <span data-ttu-id="8dee6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dee6-118">-AsJob</span></span>
<span data-ttu-id="8dee6-119">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="8dee6-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8dee6-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="8dee6-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="8dee6-121">Indica se a extensão deve usar uma versão secundária mais recente, se disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="8dee6-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="8dee6-122">Depois de implantada, no entanto, a extensão não atualizará versões secundárias, a menos que reimplantada, mesmo com essa propriedade definida como true.</span><span class="sxs-lookup"><span data-stu-id="8dee6-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="8dee6-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8dee6-123">-ClusterName</span></span>
<span data-ttu-id="8dee6-124">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="8dee6-124">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dee6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dee6-125">-DefaultProfile</span></span>
<span data-ttu-id="8dee6-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8dee6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dee6-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="8dee6-127">-ForceUpdateTag</span></span>
<span data-ttu-id="8dee6-128">Se um valor for fornecido e for diferente do valor anterior, o manipulador de extensão será forçado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="8dee6-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dee6-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dee6-129">-InputObject</span></span>
<span data-ttu-id="8dee6-130">Recurso de tipo de nó</span><span class="sxs-lookup"><span data-stu-id="8dee6-130">Node Type resource</span></span>

```yaml
Type: PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dee6-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="8dee6-131">-Name</span></span>
<span data-ttu-id="8dee6-132">nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="8dee6-132">extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dee6-133">-NodeTypename</span><span class="sxs-lookup"><span data-stu-id="8dee6-133">-NodeTypeName</span></span>
<span data-ttu-id="8dee6-134">Especifique o nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="8dee6-134">Specify the name of the node type.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dee6-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="8dee6-135">-ProtectedSetting</span></span>
<span data-ttu-id="8dee6-136">A extensão pode conter o protectedSettings ou o protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="8dee6-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dee6-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="8dee6-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="8dee6-138">Coleção de nomes de extensão após o qual essa extensão precisa ser provisionada.</span><span class="sxs-lookup"><span data-stu-id="8dee6-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dee6-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8dee6-139">-Publisher</span></span>
<span data-ttu-id="8dee6-140">O nome do fornecedor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="8dee6-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="8dee6-141">Isso pode usar o cmdlet Get-AzVMImagePublisher para obter o fornecedor.</span><span class="sxs-lookup"><span data-stu-id="8dee6-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dee6-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dee6-142">-ResourceGroupName</span></span>
<span data-ttu-id="8dee6-143">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8dee6-143">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dee6-144">-Configuração</span><span class="sxs-lookup"><span data-stu-id="8dee6-144">-Setting</span></span>
<span data-ttu-id="8dee6-145">Configurações públicas formatadas como JSON para a extensão.</span><span class="sxs-lookup"><span data-stu-id="8dee6-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dee6-146">-Digite</span><span class="sxs-lookup"><span data-stu-id="8dee6-146">-Type</span></span>
<span data-ttu-id="8dee6-147">Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="8dee6-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="8dee6-148">Você pode usar o cmdlet Get-AzVMExtensionImageType para obter o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="8dee6-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dee6-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="8dee6-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="8dee6-150">Especifica a versão do manipulador de script.</span><span class="sxs-lookup"><span data-stu-id="8dee6-150">Specifies the version of the script handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dee6-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8dee6-151">-Confirm</span></span>
<span data-ttu-id="8dee6-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dee6-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dee6-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dee6-153">-WhatIf</span></span>
<span data-ttu-id="8dee6-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8dee6-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dee6-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8dee6-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dee6-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dee6-156">CommonParameters</span></span>
<span data-ttu-id="8dee6-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dee6-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dee6-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dee6-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dee6-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8dee6-159">INPUTS</span></span>

### <span data-ttu-id="8dee6-160">System. String</span><span class="sxs-lookup"><span data-stu-id="8dee6-160">System.String</span></span>

### <span data-ttu-id="8dee6-161">Microsoft. Azure. Commands. imfabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="8dee6-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="8dee6-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8dee6-162">OUTPUTS</span></span>

### <span data-ttu-id="8dee6-163">Microsoft. Azure. Commands. imfabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="8dee6-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="8dee6-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8dee6-164">NOTES</span></span>

## <span data-ttu-id="8dee6-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8dee6-165">RELATED LINKS</span></span>
