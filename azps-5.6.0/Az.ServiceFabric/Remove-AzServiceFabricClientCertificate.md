---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: 1ed5b95346ffde947366696f30e54cfddcdea4d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892343"
---
# <span data-ttu-id="f7b72-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f7b72-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="f7b72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7b72-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b72-103">Remova um(s)(s) certificado(s) ou (s) nome(s) de certificado (s) de ser usado para autenticação do cliente para o cluster.</span><span class="sxs-lookup"><span data-stu-id="f7b72-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="f7b72-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f7b72-104">SYNTAX</span></span>

### <span data-ttu-id="f7b72-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="f7b72-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7b72-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="f7b72-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7b72-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="f7b72-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7b72-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="f7b72-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7b72-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f7b72-109">DESCRIPTION</span></span>
<span data-ttu-id="f7b72-110">Use **Remove-AzServiceFabricClientCertificate** para remover um(s) certificado(s) ou (s) nome(s) de certificado (s) de ser usado para autenticação do cliente para o cluster.</span><span class="sxs-lookup"><span data-stu-id="f7b72-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="f7b72-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7b72-111">EXAMPLES</span></span>

### <span data-ttu-id="f7b72-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f7b72-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="f7b72-113">Este comando removerá o certificado do cliente com a impressão digital '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' do cluster.</span><span class="sxs-lookup"><span data-stu-id="f7b72-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="f7b72-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f7b72-114">PARAMETERS</span></span>

### <span data-ttu-id="f7b72-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="f7b72-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="f7b72-116">Especificar a impressão digital do certificado do cliente que só tem permissão de administrador</span><span class="sxs-lookup"><span data-stu-id="f7b72-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="f7b72-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="f7b72-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="f7b72-118">Especificar o nome comum do cliente, impressão digital do emissor e tipo de autenticação</span><span class="sxs-lookup"><span data-stu-id="f7b72-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="f7b72-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="f7b72-119">-CommonName</span></span>
<span data-ttu-id="f7b72-120">Especificar o nome comum do certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="f7b72-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="f7b72-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b72-121">-DefaultProfile</span></span>
<span data-ttu-id="f7b72-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b72-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7b72-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="f7b72-123">-IssuerThumbprint</span></span>
<span data-ttu-id="f7b72-124">Especificar impressão digital do emissor do certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="f7b72-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="f7b72-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f7b72-125">-Name</span></span>
<span data-ttu-id="f7b72-126">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="f7b72-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="f7b72-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="f7b72-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="f7b72-128">Especifique a impressão digital do certificado do cliente que tem somente permissão de leitura</span><span class="sxs-lookup"><span data-stu-id="f7b72-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="f7b72-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7b72-129">-ResourceGroupName</span></span>
<span data-ttu-id="f7b72-130">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f7b72-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f7b72-131">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="f7b72-131">-Thumbprint</span></span>
<span data-ttu-id="f7b72-132">Especificar impressão digital do certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="f7b72-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="f7b72-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7b72-133">-Confirm</span></span>
<span data-ttu-id="f7b72-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7b72-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7b72-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7b72-135">-WhatIf</span></span>
<span data-ttu-id="f7b72-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f7b72-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7b72-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7b72-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7b72-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b72-138">CommonParameters</span></span>
<span data-ttu-id="f7b72-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7b72-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b72-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7b72-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b72-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7b72-141">INPUTS</span></span>

### <span data-ttu-id="f7b72-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f7b72-142">System.String</span></span>

### <span data-ttu-id="f7b72-143">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f7b72-143">System.String[]</span></span>

### <span data-ttu-id="f7b72-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="f7b72-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="f7b72-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f7b72-145">OUTPUTS</span></span>

### <span data-ttu-id="f7b72-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="f7b72-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="f7b72-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="f7b72-147">NOTES</span></span>

## <span data-ttu-id="f7b72-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7b72-148">RELATED LINKS</span></span>

[<span data-ttu-id="f7b72-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f7b72-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
