---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114503"
---
# <span data-ttu-id="4ed4d-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4ed4d-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="4ed4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ed4d-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed4d-103">Revogar o certificado do cliente por impressão digital ou nome comum.</span><span class="sxs-lookup"><span data-stu-id="4ed4d-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="4ed4d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ed4d-104">SYNTAX</span></span>

### <span data-ttu-id="4ed4d-105">ClientCertByTpByObj (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4ed4d-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ed4d-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="4ed4d-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ed4d-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="4ed4d-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ed4d-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="4ed4d-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ed4d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ed4d-109">DESCRIPTION</span></span>
<span data-ttu-id="4ed4d-110">Revogar o certificado do cliente por impressão digital ou nome comum.</span><span class="sxs-lookup"><span data-stu-id="4ed4d-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="4ed4d-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4ed4d-111">EXAMPLES</span></span>

### <span data-ttu-id="4ed4d-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4ed4d-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="4ed4d-113">Remover certificado do cliente por nome comum.</span><span class="sxs-lookup"><span data-stu-id="4ed4d-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="4ed4d-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4ed4d-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="4ed4d-115">Remover certificado do cliente por impressão digital.</span><span class="sxs-lookup"><span data-stu-id="4ed4d-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="4ed4d-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4ed4d-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="4ed4d-117">Remova o certificado do cliente por impressão digital, com canos.</span><span class="sxs-lookup"><span data-stu-id="4ed4d-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="4ed4d-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ed4d-118">PARAMETERS</span></span>

### <span data-ttu-id="4ed4d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ed4d-119">-AsJob</span></span>
<span data-ttu-id="4ed4d-120">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="4ed4d-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4ed4d-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="4ed4d-121">-CommonName</span></span>
<span data-ttu-id="4ed4d-122">Nome comum do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="4ed4d-122">Client certificate common name.</span></span>

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

### <span data-ttu-id="4ed4d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed4d-123">-DefaultProfile</span></span>
<span data-ttu-id="4ed4d-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed4d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ed4d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ed4d-125">-InputObject</span></span>
<span data-ttu-id="4ed4d-126">Recurso de cluster gerenciado</span><span class="sxs-lookup"><span data-stu-id="4ed4d-126">Managed cluster resource</span></span>

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

### <span data-ttu-id="4ed4d-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ed4d-127">-Name</span></span>
<span data-ttu-id="4ed4d-128">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="4ed4d-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4ed4d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ed4d-129">-PassThru</span></span>
<span data-ttu-id="4ed4d-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="4ed4d-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="4ed4d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ed4d-131">-ResourceGroupName</span></span>
<span data-ttu-id="4ed4d-132">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4ed4d-132">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4ed4d-133">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="4ed4d-133">-Thumbprint</span></span>
<span data-ttu-id="4ed4d-134">Impressão de miniatura do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="4ed4d-134">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="4ed4d-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4ed4d-135">-Confirm</span></span>
<span data-ttu-id="4ed4d-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ed4d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ed4d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ed4d-137">-WhatIf</span></span>
<span data-ttu-id="4ed4d-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4ed4d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ed4d-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ed4d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ed4d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed4d-140">CommonParameters</span></span>
<span data-ttu-id="4ed4d-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed4d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed4d-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ed4d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed4d-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="4ed4d-143">INPUTS</span></span>

### <span data-ttu-id="4ed4d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="4ed4d-144">System.String</span></span>

## <span data-ttu-id="4ed4d-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="4ed4d-145">OUTPUTS</span></span>

### <span data-ttu-id="4ed4d-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="4ed4d-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="4ed4d-147">Notas</span><span class="sxs-lookup"><span data-stu-id="4ed4d-147">NOTES</span></span>

## <span data-ttu-id="4ed4d-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ed4d-148">RELATED LINKS</span></span>
