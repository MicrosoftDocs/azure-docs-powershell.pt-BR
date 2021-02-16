---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: c7a88cad933781b00e720c273be467966991cebf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116379"
---
# <span data-ttu-id="f57f0-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f57f0-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="f57f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f57f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f57f0-103">Remova um(s) certificado(s) cliente(s) ou (s) nome(s) de certificado(s) de ser usado para autenticação do cliente para o cluster.</span><span class="sxs-lookup"><span data-stu-id="f57f0-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="f57f0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f57f0-104">SYNTAX</span></span>

### <span data-ttu-id="f57f0-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="f57f0-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f57f0-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="f57f0-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f57f0-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="f57f0-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f57f0-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="f57f0-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f57f0-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f57f0-109">DESCRIPTION</span></span>
<span data-ttu-id="f57f0-110">Use **Remove-AzServiceFabricClientCertificate** para remover um(s) certificado(s) cliente(s) ou (s) nome(s) de certificado (s) de ser usado para autenticação de cliente para o cluster.</span><span class="sxs-lookup"><span data-stu-id="f57f0-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="f57f0-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f57f0-111">EXAMPLES</span></span>

### <span data-ttu-id="f57f0-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f57f0-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="f57f0-113">Esse comando removerá o certificado do cliente com a impressão miniatura '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' do cluster.</span><span class="sxs-lookup"><span data-stu-id="f57f0-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="f57f0-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f57f0-114">PARAMETERS</span></span>

### <span data-ttu-id="f57f0-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="f57f0-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="f57f0-116">Especificar a impressão de certificado do cliente que só tem permissão de administrador</span><span class="sxs-lookup"><span data-stu-id="f57f0-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="f57f0-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="f57f0-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="f57f0-118">Especificar o nome comum do cliente, a impressão digital do emissor e o tipo de autenticação</span><span class="sxs-lookup"><span data-stu-id="f57f0-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="f57f0-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="f57f0-119">-CommonName</span></span>
<span data-ttu-id="f57f0-120">Especificar o nome comum do certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="f57f0-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="f57f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f57f0-121">-DefaultProfile</span></span>
<span data-ttu-id="f57f0-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f57f0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f57f0-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="f57f0-123">-IssuerThumbprint</span></span>
<span data-ttu-id="f57f0-124">Especificar a impressão digital do emissor do certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="f57f0-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="f57f0-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f57f0-125">-Name</span></span>
<span data-ttu-id="f57f0-126">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="f57f0-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="f57f0-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="f57f0-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="f57f0-128">Especificar a impressão de certificado do cliente que só tem permissão somente leitura</span><span class="sxs-lookup"><span data-stu-id="f57f0-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="f57f0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f57f0-129">-ResourceGroupName</span></span>
<span data-ttu-id="f57f0-130">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f57f0-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f57f0-131">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="f57f0-131">-Thumbprint</span></span>
<span data-ttu-id="f57f0-132">Especificar a impressão de certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="f57f0-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="f57f0-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f57f0-133">-Confirm</span></span>
<span data-ttu-id="f57f0-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f57f0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f57f0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f57f0-135">-WhatIf</span></span>
<span data-ttu-id="f57f0-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f57f0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f57f0-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f57f0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f57f0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f57f0-138">CommonParameters</span></span>
<span data-ttu-id="f57f0-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f57f0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f57f0-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f57f0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f57f0-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="f57f0-141">INPUTS</span></span>

### <span data-ttu-id="f57f0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f57f0-142">System.String</span></span>

### <span data-ttu-id="f57f0-143">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f57f0-143">System.String[]</span></span>

### <span data-ttu-id="f57f0-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="f57f0-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="f57f0-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="f57f0-145">OUTPUTS</span></span>

### <span data-ttu-id="f57f0-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="f57f0-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="f57f0-147">Notas</span><span class="sxs-lookup"><span data-stu-id="f57f0-147">NOTES</span></span>

## <span data-ttu-id="f57f0-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f57f0-148">RELATED LINKS</span></span>

[<span data-ttu-id="f57f0-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f57f0-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
