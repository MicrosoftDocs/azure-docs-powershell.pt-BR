---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: 033f96abd50e6bc5260577b78e27904e5c361a98
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599118"
---
# <span data-ttu-id="97ce4-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="97ce4-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="97ce4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="97ce4-103">Remova o (s) certificado (s) do (s) certificado (s) de cliente ou nome (s) dos (s) nome (s) da sua utilização para autenticação de cliente</span><span class="sxs-lookup"><span data-stu-id="97ce4-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="97ce4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97ce4-104">SYNTAX</span></span>

### <span data-ttu-id="97ce4-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="97ce4-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97ce4-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="97ce4-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97ce4-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="97ce4-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97ce4-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="97ce4-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97ce4-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97ce4-109">DESCRIPTION</span></span>
<span data-ttu-id="97ce4-110">Use **Remove-AzServiceFabricClientCertificate** para remover o nome (s) do (s) certificado (s) do (s) usuário (s) ou nome (s) do (s) nome (s) do (s) de usuário</span><span class="sxs-lookup"><span data-stu-id="97ce4-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="97ce4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97ce4-111">EXAMPLES</span></span>

### <span data-ttu-id="97ce4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="97ce4-112">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="97ce4-113">Esse comando removerá o certificado do cliente com a impressão digital ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' do cluster.</span><span class="sxs-lookup"><span data-stu-id="97ce4-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="97ce4-114">OS</span><span class="sxs-lookup"><span data-stu-id="97ce4-114">PARAMETERS</span></span>

### <span data-ttu-id="97ce4-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="97ce4-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="97ce4-116">Especifique a impressão digital do certificado de cliente que tem apenas permissão de administrador.</span><span class="sxs-lookup"><span data-stu-id="97ce4-116">Specify client certificate thumbprint that only has admin permission.</span></span>

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

### <span data-ttu-id="97ce4-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="97ce4-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="97ce4-118">Especifique o nome comum do cliente, a impressão digital do emissor e o tipo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="97ce4-118">Specify client common name, issuer thumbprint, and authentication type.</span></span>

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

### <span data-ttu-id="97ce4-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="97ce4-119">-CommonName</span></span>
<span data-ttu-id="97ce4-120">Especifique o nome comum do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="97ce4-120">Specify client certificate common name.</span></span>

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

### <span data-ttu-id="97ce4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97ce4-121">-DefaultProfile</span></span>
<span data-ttu-id="97ce4-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97ce4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97ce4-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="97ce4-123">-IssuerThumbprint</span></span>
<span data-ttu-id="97ce4-124">Especificar a impressão digital do emissor do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="97ce4-124">Specify client certificate issuer thumbprint.</span></span>

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

### <span data-ttu-id="97ce4-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="97ce4-125">-Name</span></span>
<span data-ttu-id="97ce4-126">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="97ce4-126">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="97ce4-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="97ce4-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="97ce4-128">Especifique a impressão digital de certificado de cliente que tem permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="97ce4-128">Specify client certificate thumbprint that has read only permission.</span></span>

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

### <span data-ttu-id="97ce4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97ce4-129">-ResourceGroupName</span></span>
<span data-ttu-id="97ce4-130">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="97ce4-130">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="97ce4-131">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="97ce4-131">-Thumbprint</span></span>
<span data-ttu-id="97ce4-132">Especifique a impressão digital do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="97ce4-132">Specify client certificate thumbprint.</span></span>

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

### <span data-ttu-id="97ce4-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="97ce4-133">-Confirm</span></span>
<span data-ttu-id="97ce4-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97ce4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97ce4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97ce4-135">-WhatIf</span></span>
<span data-ttu-id="97ce4-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97ce4-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97ce4-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97ce4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97ce4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ce4-138">CommonParameters</span></span>
<span data-ttu-id="97ce4-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97ce4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ce4-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97ce4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ce4-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97ce4-141">INPUTS</span></span>

### <span data-ttu-id="97ce4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="97ce4-142">System.String</span></span>

### <span data-ttu-id="97ce4-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="97ce4-143">System.String[]</span></span>

### <span data-ttu-id="97ce4-144">Microsoft. Azure. Commands. imfabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="97ce4-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="97ce4-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97ce4-145">OUTPUTS</span></span>

### <span data-ttu-id="97ce4-146">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="97ce4-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="97ce4-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97ce4-147">NOTES</span></span>

## <span data-ttu-id="97ce4-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97ce4-148">RELATED LINKS</span></span>

[<span data-ttu-id="97ce4-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="97ce4-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
