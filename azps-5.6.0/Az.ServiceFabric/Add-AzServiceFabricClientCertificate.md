---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: 8141b85c3322918fc955deaa6db9abb1bbf78f8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885257"
---
# <span data-ttu-id="a076a-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a076a-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="a076a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a076a-102">SYNOPSIS</span></span>
<span data-ttu-id="a076a-103">Adicione nome comum ou impressão digital ao cluster para fins de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="a076a-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="a076a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a076a-104">SYNTAX</span></span>

### <span data-ttu-id="a076a-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a076a-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a076a-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a076a-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a076a-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a076a-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a076a-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a076a-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a076a-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a076a-109">DESCRIPTION</span></span>
<span data-ttu-id="a076a-110">Use **Add-AzServiceFabricClientCertificate** para adicionar um nome comum e impressão digital de emissor ou impressão digital de certificado ao cluster, para que o cliente possa usá-la para autenticação.</span><span class="sxs-lookup"><span data-stu-id="a076a-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="a076a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a076a-111">EXAMPLES</span></span>

### <span data-ttu-id="a076a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a076a-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="a076a-113">Este comando adicionará o certificado com a impressão digital '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' ao cluster, para que o cliente possa usar o certificado como administrador para se comunicar com o cluster.</span><span class="sxs-lookup"><span data-stu-id="a076a-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="a076a-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a076a-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="a076a-115">Este comando adicionará um certificado de cliente somente leitura que tem o nome comum 'Contoso.com' e a impressão digital do emissor é '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' no cluster.</span><span class="sxs-lookup"><span data-stu-id="a076a-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="a076a-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a076a-116">PARAMETERS</span></span>

### <span data-ttu-id="a076a-117">-Admin</span><span class="sxs-lookup"><span data-stu-id="a076a-117">-Admin</span></span>
<span data-ttu-id="a076a-118">Tipo de autenticação do cliente</span><span class="sxs-lookup"><span data-stu-id="a076a-118">Client authentication type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a076a-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a076a-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="a076a-120">Especificar a impressão digital do certificado do cliente que só tem permissão de administrador</span><span class="sxs-lookup"><span data-stu-id="a076a-120">Specify client certificate thumbprint which only has admin permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a076a-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="a076a-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="a076a-122">Especificar o nome comum do cliente, impressão digital do emissor e tipo de autenticação</span><span class="sxs-lookup"><span data-stu-id="a076a-122">Specify client common name , issuer thumbprint and authentication type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a076a-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="a076a-123">-CommonName</span></span>
<span data-ttu-id="a076a-124">Especificar o nome comum do certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="a076a-124">Specify client certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a076a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a076a-125">-DefaultProfile</span></span>
<span data-ttu-id="a076a-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a076a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a076a-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="a076a-127">-IssuerThumbprint</span></span>
<span data-ttu-id="a076a-128">Especificar impressão digital do emissor do certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="a076a-128">Specify thumbprint of client certificate's issuer</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a076a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="a076a-129">-Name</span></span>
<span data-ttu-id="a076a-130">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="a076a-130">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a076a-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a076a-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="a076a-132">Especifique a impressão digital do certificado do cliente que tem somente permissão de leitura</span><span class="sxs-lookup"><span data-stu-id="a076a-132">Specify client certificate thumbprint which only has read only permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a076a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a076a-133">-ResourceGroupName</span></span>
<span data-ttu-id="a076a-134">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a076a-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a076a-135">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="a076a-135">-Thumbprint</span></span>
<span data-ttu-id="a076a-136">Especificar impressão digital do certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="a076a-136">Specify client certificate thumbprint</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a076a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a076a-137">-Confirm</span></span>
<span data-ttu-id="a076a-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a076a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a076a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a076a-139">-WhatIf</span></span>
<span data-ttu-id="a076a-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a076a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a076a-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a076a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a076a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a076a-142">CommonParameters</span></span>
<span data-ttu-id="a076a-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a076a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a076a-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a076a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a076a-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a076a-145">INPUTS</span></span>

### <span data-ttu-id="a076a-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a076a-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a076a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="a076a-147">System.String</span></span>

### <span data-ttu-id="a076a-148">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a076a-148">System.String[]</span></span>

### <span data-ttu-id="a076a-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="a076a-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="a076a-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a076a-150">OUTPUTS</span></span>

### <span data-ttu-id="a076a-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="a076a-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a076a-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="a076a-152">NOTES</span></span>

## <span data-ttu-id="a076a-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a076a-153">RELATED LINKS</span></span>

[<span data-ttu-id="a076a-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a076a-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
