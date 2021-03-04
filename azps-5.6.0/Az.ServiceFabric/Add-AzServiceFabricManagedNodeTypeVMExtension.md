---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: 14138dddcd4f4b2150377726d862d953c7360a31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887613"
---
# <span data-ttu-id="4c7ef-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="4c7ef-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="4c7ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c7ef-102">SYNOPSIS</span></span>
<span data-ttu-id="4c7ef-103">Adicione extensão vm ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="4c7ef-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4c7ef-104">SYNTAX</span></span>

### <span data-ttu-id="4c7ef-105">ByObj (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4c7ef-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c7ef-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4c7ef-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c7ef-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4c7ef-107">DESCRIPTION</span></span>
<span data-ttu-id="4c7ef-108">Adicione extensão vm ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-108">Add vm extension to the node type.</span></span> <span data-ttu-id="4c7ef-109">Isso adicionará a extensão ao recurso Conjunto de Escala de Máquina Virtual subliying.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="4c7ef-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c7ef-110">EXAMPLES</span></span>

### <span data-ttu-id="4c7ef-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4c7ef-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="4c7ef-112">Este comando adiciona uma extensão ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="4c7ef-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4c7ef-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="4c7ef-114">Este comando adiciona uma extensão com configurações e configurações protegidas ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="4c7ef-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4c7ef-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="4c7ef-116">Este comando adiciona uma extensão ao tipo de nó, com canalização.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="4c7ef-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4c7ef-117">PARAMETERS</span></span>

### <span data-ttu-id="4c7ef-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c7ef-118">-AsJob</span></span>
<span data-ttu-id="4c7ef-119">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4c7ef-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="4c7ef-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="4c7ef-121">Indica se a extensão deve usar uma versão secundária mais recente se uma estiver disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="4c7ef-122">No entanto, uma vez implantado, a extensão não atualizará versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como true.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="4c7ef-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4c7ef-123">-ClusterName</span></span>
<span data-ttu-id="4c7ef-124">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4c7ef-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c7ef-125">-DefaultProfile</span></span>
<span data-ttu-id="4c7ef-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c7ef-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="4c7ef-127">-ForceUpdateTag</span></span>
<span data-ttu-id="4c7ef-128">Se um valor for fornecido e for diferente do valor anterior, o manipulador de extensão será forçado a atualizar mesmo que a configuração da extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="4c7ef-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c7ef-129">-InputObject</span></span>
<span data-ttu-id="4c7ef-130">Recurso Tipo de Nó</span><span class="sxs-lookup"><span data-stu-id="4c7ef-130">Node Type resource</span></span>

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

### <span data-ttu-id="4c7ef-131">-Name</span><span class="sxs-lookup"><span data-stu-id="4c7ef-131">-Name</span></span>
<span data-ttu-id="4c7ef-132">nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-132">extension name.</span></span>

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

### <span data-ttu-id="4c7ef-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="4c7ef-133">-NodeTypeName</span></span>
<span data-ttu-id="4c7ef-134">Especifique o nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-134">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="4c7ef-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="4c7ef-135">-ProtectedSetting</span></span>
<span data-ttu-id="4c7ef-136">A extensão pode conter protectedSettings ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="4c7ef-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="4c7ef-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="4c7ef-138">Coleção de nomes de extensão após os quais essa extensão precisa ser provisionada.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="4c7ef-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="4c7ef-139">-Publisher</span></span>
<span data-ttu-id="4c7ef-140">O nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="4c7ef-141">Isso pode usar o cmdlet Get-AzVMImagePublisher para obter o editor.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="4c7ef-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c7ef-142">-ResourceGroupName</span></span>
<span data-ttu-id="4c7ef-143">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-143">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4c7ef-144">-Setting</span><span class="sxs-lookup"><span data-stu-id="4c7ef-144">-Setting</span></span>
<span data-ttu-id="4c7ef-145">Configurações públicas formatadas Json para a extensão.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="4c7ef-146">-Type</span><span class="sxs-lookup"><span data-stu-id="4c7ef-146">-Type</span></span>
<span data-ttu-id="4c7ef-147">Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="4c7ef-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="4c7ef-148">Você pode usar o cmdlet Get-AzVMExtensionImageType para obter o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="4c7ef-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="4c7ef-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="4c7ef-150">Especifica a versão do manipulador de scripts.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-150">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="4c7ef-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c7ef-151">-Confirm</span></span>
<span data-ttu-id="4c7ef-152">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c7ef-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c7ef-153">-WhatIf</span></span>
<span data-ttu-id="4c7ef-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c7ef-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c7ef-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c7ef-156">CommonParameters</span></span>
<span data-ttu-id="4c7ef-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c7ef-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c7ef-158">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c7ef-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c7ef-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c7ef-159">INPUTS</span></span>

### <span data-ttu-id="4c7ef-160">System.String</span><span class="sxs-lookup"><span data-stu-id="4c7ef-160">System.String</span></span>

### <span data-ttu-id="4c7ef-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="4c7ef-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="4c7ef-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4c7ef-162">OUTPUTS</span></span>

### <span data-ttu-id="4c7ef-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="4c7ef-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="4c7ef-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="4c7ef-164">NOTES</span></span>

## <span data-ttu-id="4c7ef-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c7ef-165">RELATED LINKS</span></span>
