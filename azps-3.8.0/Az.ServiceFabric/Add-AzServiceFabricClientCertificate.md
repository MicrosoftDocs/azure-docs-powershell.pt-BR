---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: 913b610bc1d79c7a1792c06b53947fd3bf51151a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940873"
---
# <span data-ttu-id="af731-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="af731-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="af731-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af731-102">SYNOPSIS</span></span>
<span data-ttu-id="af731-103">Adicione um nome comum ou impressão digital ao cluster para fins de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="af731-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="af731-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af731-104">SYNTAX</span></span>

### <span data-ttu-id="af731-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="af731-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af731-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="af731-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af731-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="af731-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af731-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="af731-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af731-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af731-109">DESCRIPTION</span></span>
<span data-ttu-id="af731-110">Use **Add-AzServiceFabricClientCertificate** para adicionar um nome comum e uma impressão digital do emissor ou impressão digital de certificado ao cluster, para que o cliente possa usá-lo para autenticação.</span><span class="sxs-lookup"><span data-stu-id="af731-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="af731-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af731-111">EXAMPLES</span></span>

### <span data-ttu-id="af731-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af731-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="af731-113">Esse comando adicionará o certificado com a impressão digital ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' ao cluster, portanto, o cliente poderá usar o certificado como administrador para se comunicar com o cluster.</span><span class="sxs-lookup"><span data-stu-id="af731-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="af731-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="af731-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="af731-115">Esse comando adicionará um certificado de cliente somente leitura que é o nome comum é ' Contoso.com ' e a impressão digital do emissor é ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' para o cluster.</span><span class="sxs-lookup"><span data-stu-id="af731-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="af731-116">OS</span><span class="sxs-lookup"><span data-stu-id="af731-116">PARAMETERS</span></span>

### <span data-ttu-id="af731-117">-Administrador</span><span class="sxs-lookup"><span data-stu-id="af731-117">-Admin</span></span>
<span data-ttu-id="af731-118">Tipo de autenticação do cliente</span><span class="sxs-lookup"><span data-stu-id="af731-118">Client authentication type</span></span>

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

### <span data-ttu-id="af731-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="af731-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="af731-120">Especificar a impressão digital do certificado de cliente que tem apenas permissão de administrador</span><span class="sxs-lookup"><span data-stu-id="af731-120">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="af731-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="af731-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="af731-122">Especificar o nome comum do cliente, a impressão digital do emissor e o tipo de autenticação</span><span class="sxs-lookup"><span data-stu-id="af731-122">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="af731-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="af731-123">-CommonName</span></span>
<span data-ttu-id="af731-124">Especificar nome comum do certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="af731-124">Specify client certificate common name</span></span>

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

### <span data-ttu-id="af731-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af731-125">-DefaultProfile</span></span>
<span data-ttu-id="af731-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af731-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af731-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="af731-127">-IssuerThumbprint</span></span>
<span data-ttu-id="af731-128">Especificar a impressão digital do emissor do certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="af731-128">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="af731-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="af731-129">-Name</span></span>
<span data-ttu-id="af731-130">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="af731-130">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="af731-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="af731-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="af731-132">Especificar a impressão digital do certificado de cliente que tem apenas permissão somente leitura</span><span class="sxs-lookup"><span data-stu-id="af731-132">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="af731-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af731-133">-ResourceGroupName</span></span>
<span data-ttu-id="af731-134">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="af731-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="af731-135">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="af731-135">-Thumbprint</span></span>
<span data-ttu-id="af731-136">Especificar a impressão digital do certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="af731-136">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="af731-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af731-137">-Confirm</span></span>
<span data-ttu-id="af731-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af731-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af731-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af731-139">-WhatIf</span></span>
<span data-ttu-id="af731-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af731-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af731-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af731-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af731-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af731-142">CommonParameters</span></span>
<span data-ttu-id="af731-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af731-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af731-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af731-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af731-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af731-145">INPUTS</span></span>

### <span data-ttu-id="af731-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="af731-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="af731-147">System. String</span><span class="sxs-lookup"><span data-stu-id="af731-147">System.String</span></span>

### <span data-ttu-id="af731-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="af731-148">System.String[]</span></span>

### <span data-ttu-id="af731-149">Microsoft. Azure. Commands. imfabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="af731-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="af731-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af731-150">OUTPUTS</span></span>

### <span data-ttu-id="af731-151">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="af731-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="af731-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af731-152">NOTES</span></span>

## <span data-ttu-id="af731-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af731-153">RELATED LINKS</span></span>

[<span data-ttu-id="af731-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="af731-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
