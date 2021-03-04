---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 98e160253db571c32fe14455b8642337029a9707
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887077"
---
# <span data-ttu-id="e5ada-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5ada-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="e5ada-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5ada-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ada-103">Cria uma configuração de nome de host para o Gateway existente.</span><span class="sxs-lookup"><span data-stu-id="e5ada-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="e5ada-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e5ada-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5ada-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e5ada-105">DESCRIPTION</span></span>
<span data-ttu-id="e5ada-106">O cmdlet **New-AzApiManagementGatewayHostnameConfiguration** cria uma configuração de nome de host para o Gateway existente.</span><span class="sxs-lookup"><span data-stu-id="e5ada-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="e5ada-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5ada-107">EXAMPLES</span></span>

### <span data-ttu-id="e5ada-108">Exemplo 1: Criar uma configuração de nome de host para o gateway existente</span><span class="sxs-lookup"><span data-stu-id="e5ada-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="e5ada-109">Este comando cria uma configuração de nome de host "h01" para um gateway "g01".</span><span class="sxs-lookup"><span data-stu-id="e5ada-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="e5ada-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e5ada-110">PARAMETERS</span></span>

### <span data-ttu-id="e5ada-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="e5ada-111">-CertificateResourceId</span></span>
<span data-ttu-id="e5ada-112">Um identificador de recurso para a id de certificado existente. Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e5ada-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5ada-113">-Context</span><span class="sxs-lookup"><span data-stu-id="e5ada-113">-Context</span></span>
<span data-ttu-id="e5ada-114">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e5ada-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e5ada-115">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e5ada-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5ada-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ada-116">-DefaultProfile</span></span>
<span data-ttu-id="e5ada-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5ada-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5ada-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e5ada-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="e5ada-119">Identificador da nova configuração de nome de host do gateway.</span><span class="sxs-lookup"><span data-stu-id="e5ada-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="e5ada-120">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e5ada-120">This parameter is optional.</span></span>
<span data-ttu-id="e5ada-121">Se não for especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="e5ada-121">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5ada-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e5ada-122">-GatewayId</span></span>
<span data-ttu-id="e5ada-123">Identificador do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="e5ada-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="e5ada-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e5ada-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5ada-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="e5ada-125">-Hostname</span></span>
<span data-ttu-id="e5ada-126">Nomedo host.</span><span class="sxs-lookup"><span data-stu-id="e5ada-126">Hostname.</span></span>
<span data-ttu-id="e5ada-127">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e5ada-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5ada-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e5ada-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="e5ada-129">Sinalizador para impor NegotiateClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="e5ada-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="e5ada-130">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e5ada-130">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5ada-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5ada-131">-Confirm</span></span>
<span data-ttu-id="e5ada-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5ada-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5ada-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5ada-133">-WhatIf</span></span>
<span data-ttu-id="e5ada-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e5ada-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5ada-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5ada-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5ada-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ada-136">CommonParameters</span></span>
<span data-ttu-id="e5ada-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5ada-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ada-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5ada-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ada-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5ada-139">INPUTS</span></span>

### <span data-ttu-id="e5ada-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e5ada-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e5ada-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e5ada-141">System.String</span></span>

### <span data-ttu-id="e5ada-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e5ada-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e5ada-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e5ada-143">OUTPUTS</span></span>

### <span data-ttu-id="e5ada-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5ada-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="e5ada-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="e5ada-145">NOTES</span></span>

## <span data-ttu-id="e5ada-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5ada-146">RELATED LINKS</span></span>
