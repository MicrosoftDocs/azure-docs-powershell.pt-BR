---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: f0ba5cb4d461bbc70ba742ae46ba4b9489923545
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892337"
---
# <span data-ttu-id="d2295-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d2295-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="d2295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2295-102">SYNOPSIS</span></span>
<span data-ttu-id="d2295-103">Remvoe o certificado do cliente por impressão digital ou nome comum.</span><span class="sxs-lookup"><span data-stu-id="d2295-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="d2295-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d2295-104">SYNTAX</span></span>

### <span data-ttu-id="d2295-105">ClientCertByTpByObj (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d2295-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2295-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="d2295-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2295-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="d2295-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2295-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="d2295-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2295-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d2295-109">DESCRIPTION</span></span>
<span data-ttu-id="d2295-110">Remvoe o certificado do cliente por impressão digital ou nome comum.</span><span class="sxs-lookup"><span data-stu-id="d2295-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="d2295-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2295-111">EXAMPLES</span></span>

### <span data-ttu-id="d2295-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2295-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="d2295-113">Remover certificado de cliente por nome comum.</span><span class="sxs-lookup"><span data-stu-id="d2295-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="d2295-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d2295-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="d2295-115">Remova o certificado do cliente por impressão digital.</span><span class="sxs-lookup"><span data-stu-id="d2295-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="d2295-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d2295-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="d2295-117">Remova o certificado do cliente por impressão digital, com canalização.</span><span class="sxs-lookup"><span data-stu-id="d2295-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="d2295-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d2295-118">PARAMETERS</span></span>

### <span data-ttu-id="d2295-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2295-119">-AsJob</span></span>
<span data-ttu-id="d2295-120">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="d2295-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d2295-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="d2295-121">-CommonName</span></span>
<span data-ttu-id="d2295-122">Nome comum do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="d2295-122">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2295-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2295-123">-DefaultProfile</span></span>
<span data-ttu-id="d2295-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2295-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2295-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2295-125">-InputObject</span></span>
<span data-ttu-id="d2295-126">Recurso de cluster gerenciado</span><span class="sxs-lookup"><span data-stu-id="d2295-126">Managed cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ClientCertByTpByObj, ClientCertByCnByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2295-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d2295-127">-Name</span></span>
<span data-ttu-id="d2295-128">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="d2295-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2295-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2295-129">-PassThru</span></span>
<span data-ttu-id="d2295-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="d2295-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d2295-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2295-131">-ResourceGroupName</span></span>
<span data-ttu-id="d2295-132">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2295-132">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2295-133">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="d2295-133">-Thumbprint</span></span>
<span data-ttu-id="d2295-134">Impressão digital do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="d2295-134">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByCnTpName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2295-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2295-135">-Confirm</span></span>
<span data-ttu-id="d2295-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2295-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2295-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2295-137">-WhatIf</span></span>
<span data-ttu-id="d2295-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2295-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2295-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2295-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2295-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2295-140">CommonParameters</span></span>
<span data-ttu-id="d2295-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2295-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2295-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2295-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2295-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2295-143">INPUTS</span></span>

### <span data-ttu-id="d2295-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d2295-144">System.String</span></span>

## <span data-ttu-id="d2295-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d2295-145">OUTPUTS</span></span>

### <span data-ttu-id="d2295-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d2295-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="d2295-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="d2295-147">NOTES</span></span>

## <span data-ttu-id="d2295-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2295-148">RELATED LINKS</span></span>
