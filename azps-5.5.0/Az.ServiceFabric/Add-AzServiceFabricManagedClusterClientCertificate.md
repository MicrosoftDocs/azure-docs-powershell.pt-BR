---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113993"
---
# <span data-ttu-id="433c2-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="433c2-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="433c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="433c2-102">SYNOPSIS</span></span>
<span data-ttu-id="433c2-103">Adicione o nome comum do certificado ou a impressão digital ao cluster.</span><span class="sxs-lookup"><span data-stu-id="433c2-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="433c2-104">Isso registrará o certificado novamente no cluster para fins de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="433c2-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="433c2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="433c2-105">SYNTAX</span></span>

### <span data-ttu-id="433c2-106">ClientCertByTpByObj (Padrão)</span><span class="sxs-lookup"><span data-stu-id="433c2-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="433c2-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="433c2-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="433c2-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="433c2-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="433c2-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="433c2-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="433c2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="433c2-110">DESCRIPTION</span></span>
<span data-ttu-id="433c2-111">Adicione o nome comum do certificado ou a impressão digital ao cluster.</span><span class="sxs-lookup"><span data-stu-id="433c2-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="433c2-112">Isso registrará o certificado novamente no cluster para fins de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="433c2-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="433c2-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="433c2-113">EXAMPLES</span></span>

### <span data-ttu-id="433c2-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="433c2-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="433c2-115">Esse comando adicionará o certificado com a impressão de miniatura '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' ao cluster, para que o cliente possa usar o certificado como administrador para se comunicar com o cluster.</span><span class="sxs-lookup"><span data-stu-id="433c2-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="433c2-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="433c2-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="433c2-117">Esse comando adicionará um certificado de cliente somente leitura com o nome comum "Contoso.com" e 2 emissores.</span><span class="sxs-lookup"><span data-stu-id="433c2-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="433c2-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="433c2-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="433c2-119">Esse comando adicionará um certificado de cliente somente leitura com o nome comum "Contoso.com" e 2 emissores, com piping.</span><span class="sxs-lookup"><span data-stu-id="433c2-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="433c2-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="433c2-120">PARAMETERS</span></span>

### <span data-ttu-id="433c2-121">-Administrador</span><span class="sxs-lookup"><span data-stu-id="433c2-121">-Admin</span></span>
<span data-ttu-id="433c2-122">Use para especificar se o certificado do cliente tem nível de administrador.</span><span class="sxs-lookup"><span data-stu-id="433c2-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="433c2-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="433c2-123">-AsJob</span></span>
<span data-ttu-id="433c2-124">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="433c2-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="433c2-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="433c2-125">-CommonName</span></span>
<span data-ttu-id="433c2-126">Nome comum do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="433c2-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="433c2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="433c2-127">-DefaultProfile</span></span>
<span data-ttu-id="433c2-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="433c2-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="433c2-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="433c2-129">-InputObject</span></span>
<span data-ttu-id="433c2-130">Recurso de cluster gerenciado</span><span class="sxs-lookup"><span data-stu-id="433c2-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="433c2-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="433c2-131">-IssuerThumbprint</span></span>
<span data-ttu-id="433c2-132">Lista de miniaturas de Emissor para o certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="433c2-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="433c2-133">Use somente em combinação com CommonName.</span><span class="sxs-lookup"><span data-stu-id="433c2-133">Only use in combination with CommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="433c2-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="433c2-134">-Name</span></span>
<span data-ttu-id="433c2-135">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="433c2-135">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="433c2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="433c2-136">-ResourceGroupName</span></span>
<span data-ttu-id="433c2-137">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="433c2-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="433c2-138">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="433c2-138">-Thumbprint</span></span>
<span data-ttu-id="433c2-139">Impressão de miniatura do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="433c2-139">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByTpByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="433c2-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="433c2-140">-Confirm</span></span>
<span data-ttu-id="433c2-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="433c2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="433c2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="433c2-142">-WhatIf</span></span>
<span data-ttu-id="433c2-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="433c2-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="433c2-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="433c2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="433c2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="433c2-145">CommonParameters</span></span>
<span data-ttu-id="433c2-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="433c2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="433c2-147">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="433c2-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="433c2-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="433c2-148">INPUTS</span></span>

### <span data-ttu-id="433c2-149">System.String</span><span class="sxs-lookup"><span data-stu-id="433c2-149">System.String</span></span>

## <span data-ttu-id="433c2-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="433c2-150">OUTPUTS</span></span>

### <span data-ttu-id="433c2-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="433c2-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="433c2-152">Notas</span><span class="sxs-lookup"><span data-stu-id="433c2-152">NOTES</span></span>

## <span data-ttu-id="433c2-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="433c2-153">RELATED LINKS</span></span>
