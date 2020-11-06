---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: c7b6e00ccbe368267fd6b110490df4f70b2229a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432397"
---
# <span data-ttu-id="e008e-101">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e008e-101">Add-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="e008e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e008e-102">SYNOPSIS</span></span>
<span data-ttu-id="e008e-103">Adicione um nome comum ou impressão digital ao cluster para fins de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="e008e-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e008e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e008e-104">SYNTAX</span></span>

### <span data-ttu-id="e008e-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="e008e-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e008e-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="e008e-106">SingleUpdateWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e008e-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="e008e-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e008e-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="e008e-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e008e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e008e-109">DESCRIPTION</span></span>
<span data-ttu-id="e008e-110">Use **Add-AzureRmServiceFabricClientCertificate** para adicionar um nome comum e uma impressão digital do emissor ou impressão digital de certificado ao cluster, para que o cliente possa usá-lo para autenticação.</span><span class="sxs-lookup"><span data-stu-id="e008e-110">Use **Add-AzureRmServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="e008e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e008e-111">EXAMPLES</span></span>

### <span data-ttu-id="e008e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e008e-112">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="e008e-113">Esse comando adicionará o certificado com a impressão digital ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' ao cluster, portanto, o cliente poderá usar o certificado como administrador para se comunicar com o cluster.</span><span class="sxs-lookup"><span data-stu-id="e008e-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="e008e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e008e-114">Example 2</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="e008e-115">Esse comando adicionará um certificado de cliente somente leitura que é o nome comum é ' Contoso.com ' e a impressão digital do emissor é ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' para o cluster.</span><span class="sxs-lookup"><span data-stu-id="e008e-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="e008e-116">OS</span><span class="sxs-lookup"><span data-stu-id="e008e-116">PARAMETERS</span></span>

### <span data-ttu-id="e008e-117">-Administrador</span><span class="sxs-lookup"><span data-stu-id="e008e-117">-Admin</span></span>
<span data-ttu-id="e008e-118">Tipo de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="e008e-118">Client authentication type.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e008e-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="e008e-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="e008e-120">Especifique a impressão digital do certificado de cliente que tem apenas permissão de administrador.</span><span class="sxs-lookup"><span data-stu-id="e008e-120">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e008e-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="e008e-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="e008e-122">Especifique o nome comum do cliente, a impressão digital do emissor e o tipo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="e008e-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e008e-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="e008e-123">-CommonName</span></span>
<span data-ttu-id="e008e-124">Especifique o nome comum do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="e008e-124">Specify client certificate common name.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e008e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e008e-125">-DefaultProfile</span></span>
<span data-ttu-id="e008e-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e008e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e008e-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="e008e-127">-IssuerThumbprint</span></span>
<span data-ttu-id="e008e-128">Especificar a impressão digital do emissor do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="e008e-128">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e008e-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="e008e-129">-Name</span></span>
<span data-ttu-id="e008e-130">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="e008e-130">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e008e-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="e008e-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="e008e-132">Especifique a impressão digital de certificado de cliente que tem permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e008e-132">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e008e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e008e-133">-ResourceGroupName</span></span>
<span data-ttu-id="e008e-134">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e008e-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e008e-135">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="e008e-135">-Thumbprint</span></span>
<span data-ttu-id="e008e-136">Especifique a impressão digital do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="e008e-136">Specify client certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e008e-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e008e-137">-Confirm</span></span>
<span data-ttu-id="e008e-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e008e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e008e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e008e-139">-WhatIf</span></span>
<span data-ttu-id="e008e-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e008e-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e008e-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e008e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e008e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e008e-142">CommonParameters</span></span>
<span data-ttu-id="e008e-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e008e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e008e-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e008e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e008e-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e008e-145">INPUTS</span></span>

### <span data-ttu-id="e008e-146">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e008e-146">System.Collections.Hashtable</span></span>
<span data-ttu-id="e008e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e008e-147">System.String</span></span>

<span data-ttu-id="e008e-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e008e-148">System.Boolean</span></span>

## <span data-ttu-id="e008e-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e008e-149">OUTPUTS</span></span>

### <span data-ttu-id="e008e-150">Microsoft. Azure. Commands. imfabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="e008e-150">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="e008e-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e008e-151">NOTES</span></span>

## <span data-ttu-id="e008e-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e008e-152">RELATED LINKS</span></span>

[<span data-ttu-id="e008e-153">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e008e-153">Remove-AzureRmServiceFabricClientCertificate</span></span>](./Remove-AzureRmServiceFabricClientCertificate.md)
