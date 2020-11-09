---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: c7a88cad933781b00e720c273be467966991cebf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281719"
---
# <span data-ttu-id="54116-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="54116-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="54116-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54116-102">SYNOPSIS</span></span>
<span data-ttu-id="54116-103">Remova o (s) certificado (s) do (s) certificado (s) de cliente ou nome (s) dos (s) nome (s) da sua utilização para autenticação de cliente</span><span class="sxs-lookup"><span data-stu-id="54116-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="54116-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54116-104">SYNTAX</span></span>

### <span data-ttu-id="54116-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="54116-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54116-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="54116-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54116-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="54116-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54116-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="54116-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54116-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54116-109">DESCRIPTION</span></span>
<span data-ttu-id="54116-110">Use **Remove-AzServiceFabricClientCertificate** para remover o nome (s) do (s) certificado (s) do (s) usuário (s) ou nome (s) do (s) nome (s) do (s) de usuário</span><span class="sxs-lookup"><span data-stu-id="54116-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="54116-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54116-111">EXAMPLES</span></span>

### <span data-ttu-id="54116-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="54116-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="54116-113">Esse comando removerá o certificado do cliente com a impressão digital ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' do cluster.</span><span class="sxs-lookup"><span data-stu-id="54116-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="54116-114">OS</span><span class="sxs-lookup"><span data-stu-id="54116-114">PARAMETERS</span></span>

### <span data-ttu-id="54116-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="54116-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="54116-116">Especificar a impressão digital do certificado de cliente que tem apenas permissão de administrador</span><span class="sxs-lookup"><span data-stu-id="54116-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="54116-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="54116-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="54116-118">Especificar o nome comum do cliente, a impressão digital do emissor e o tipo de autenticação</span><span class="sxs-lookup"><span data-stu-id="54116-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="54116-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="54116-119">-CommonName</span></span>
<span data-ttu-id="54116-120">Especificar nome comum do certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="54116-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="54116-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54116-121">-DefaultProfile</span></span>
<span data-ttu-id="54116-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="54116-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54116-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="54116-123">-IssuerThumbprint</span></span>
<span data-ttu-id="54116-124">Especificar a impressão digital do emissor do certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="54116-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="54116-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="54116-125">-Name</span></span>
<span data-ttu-id="54116-126">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="54116-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="54116-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="54116-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="54116-128">Especificar a impressão digital do certificado de cliente que tem apenas permissão somente leitura</span><span class="sxs-lookup"><span data-stu-id="54116-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="54116-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54116-129">-ResourceGroupName</span></span>
<span data-ttu-id="54116-130">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="54116-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="54116-131">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="54116-131">-Thumbprint</span></span>
<span data-ttu-id="54116-132">Especificar a impressão digital do certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="54116-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="54116-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="54116-133">-Confirm</span></span>
<span data-ttu-id="54116-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54116-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54116-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54116-135">-WhatIf</span></span>
<span data-ttu-id="54116-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="54116-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54116-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="54116-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54116-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54116-138">CommonParameters</span></span>
<span data-ttu-id="54116-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54116-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54116-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54116-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54116-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54116-141">INPUTS</span></span>

### <span data-ttu-id="54116-142">System. String</span><span class="sxs-lookup"><span data-stu-id="54116-142">System.String</span></span>

### <span data-ttu-id="54116-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="54116-143">System.String[]</span></span>

### <span data-ttu-id="54116-144">Microsoft. Azure. Commands. imfabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="54116-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="54116-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54116-145">OUTPUTS</span></span>

### <span data-ttu-id="54116-146">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="54116-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="54116-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54116-147">NOTES</span></span>

## <span data-ttu-id="54116-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54116-148">RELATED LINKS</span></span>

[<span data-ttu-id="54116-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="54116-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
