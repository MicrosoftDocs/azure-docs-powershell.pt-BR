---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: e508afc5ab66a3e2aec49131bf2c8bf0e9d31259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602353"
---
# <span data-ttu-id="2449a-101">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2449a-101">Remove-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="2449a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2449a-102">SYNOPSIS</span></span>
<span data-ttu-id="2449a-103">Remova o (s) certificado (s) do (s) certificado (s) de cliente ou nome (s) dos (s) nome (s) da sua utilização para autenticação de cliente</span><span class="sxs-lookup"><span data-stu-id="2449a-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2449a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2449a-104">SYNTAX</span></span>

### <span data-ttu-id="2449a-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="2449a-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2449a-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="2449a-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2449a-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="2449a-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2449a-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="2449a-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2449a-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2449a-109">DESCRIPTION</span></span>
<span data-ttu-id="2449a-110">Use **Remove-AzureRmServiceFabricClientCertificate** para remover o nome (s) do (s) certificado (s) do (s) usuário (s) ou nome (s) do (s) nome (s) do (s) de usuário</span><span class="sxs-lookup"><span data-stu-id="2449a-110">Use **Remove-AzureRmServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="2449a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2449a-111">EXAMPLES</span></span>

### <span data-ttu-id="2449a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2449a-112">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="2449a-113">Esse comando removerá o certificado do cliente com a impressão digital ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' do cluster.</span><span class="sxs-lookup"><span data-stu-id="2449a-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="2449a-114">OS</span><span class="sxs-lookup"><span data-stu-id="2449a-114">PARAMETERS</span></span>

### <span data-ttu-id="2449a-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="2449a-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="2449a-116">Especifique a impressão digital do certificado de cliente que tem apenas permissão de administrador.</span><span class="sxs-lookup"><span data-stu-id="2449a-116">Specify client certificate thumbprint that only has admin permission.</span></span>

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

### <span data-ttu-id="2449a-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="2449a-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="2449a-118">Especifique o nome comum do cliente, a impressão digital do emissor e o tipo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="2449a-118">Specify client common name, issuer thumbprint, and authentication type.</span></span>

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

### <span data-ttu-id="2449a-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="2449a-119">-CommonName</span></span>
<span data-ttu-id="2449a-120">Especifique o nome comum do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="2449a-120">Specify client certificate common name.</span></span>

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

### <span data-ttu-id="2449a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2449a-121">-DefaultProfile</span></span>
<span data-ttu-id="2449a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2449a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2449a-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="2449a-123">-IssuerThumbprint</span></span>
<span data-ttu-id="2449a-124">Especificar a impressão digital do emissor do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="2449a-124">Specify client certificate issuer thumbprint.</span></span>

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

### <span data-ttu-id="2449a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="2449a-125">-Name</span></span>
<span data-ttu-id="2449a-126">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="2449a-126">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2449a-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="2449a-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="2449a-128">Especifique a impressão digital de certificado de cliente que tem permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="2449a-128">Specify client certificate thumbprint that has read only permission.</span></span>

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

### <span data-ttu-id="2449a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2449a-129">-ResourceGroupName</span></span>
<span data-ttu-id="2449a-130">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2449a-130">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2449a-131">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="2449a-131">-Thumbprint</span></span>
<span data-ttu-id="2449a-132">Especifique a impressão digital do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="2449a-132">Specify client certificate thumbprint.</span></span>

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

### <span data-ttu-id="2449a-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2449a-133">-Confirm</span></span>
<span data-ttu-id="2449a-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2449a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2449a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2449a-135">-WhatIf</span></span>
<span data-ttu-id="2449a-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2449a-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2449a-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2449a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2449a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2449a-138">CommonParameters</span></span>
<span data-ttu-id="2449a-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2449a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2449a-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2449a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2449a-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2449a-141">INPUTS</span></span>

### <span data-ttu-id="2449a-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2449a-142">System.Collections.Hashtable</span></span>
<span data-ttu-id="2449a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2449a-143">System.String</span></span>

<span data-ttu-id="2449a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2449a-144">System.Boolean</span></span>

## <span data-ttu-id="2449a-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2449a-145">OUTPUTS</span></span>

### <span data-ttu-id="2449a-146">Microsoft. Azure. Commands. imfabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="2449a-146">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="2449a-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2449a-147">NOTES</span></span>

## <span data-ttu-id="2449a-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2449a-148">RELATED LINKS</span></span>

[<span data-ttu-id="2449a-149">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2449a-149">Add-AzureRmServiceFabricClientCertificate</span></span>](./Add-AzureRmServiceFabricClientCertificate.md)
