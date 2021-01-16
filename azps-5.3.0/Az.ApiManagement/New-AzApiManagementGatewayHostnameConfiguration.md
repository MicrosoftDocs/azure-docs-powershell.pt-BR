---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 6aadf94ff379df322907be66c73052196de803c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432650"
---
# <span data-ttu-id="18f15-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="18f15-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="18f15-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18f15-102">SYNOPSIS</span></span>
<span data-ttu-id="18f15-103">Cria um configuratin de nome de host para o gateway existente.</span><span class="sxs-lookup"><span data-stu-id="18f15-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="18f15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18f15-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18f15-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18f15-105">DESCRIPTION</span></span>
<span data-ttu-id="18f15-106">O cmdlet **New-AzApiManagementGatewayHostnameConfiguration** cria um nome de host configuratin para o gateway existente.</span><span class="sxs-lookup"><span data-stu-id="18f15-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="18f15-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18f15-107">EXAMPLES</span></span>

### <span data-ttu-id="18f15-108">Exemplo 1: criar uma configuração de nome de host para o gateway existente</span><span class="sxs-lookup"><span data-stu-id="18f15-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="18f15-109">Esse comando cria uma configuração do nome do host "H01" para um gateway "G01".</span><span class="sxs-lookup"><span data-stu-id="18f15-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="18f15-110">OS</span><span class="sxs-lookup"><span data-stu-id="18f15-110">PARAMETERS</span></span>

### <span data-ttu-id="18f15-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="18f15-111">-CertificateResourceId</span></span>
<span data-ttu-id="18f15-112">Um identificador de recurso para a ID de certificado existente. Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="18f15-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

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

### <span data-ttu-id="18f15-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="18f15-113">-Context</span></span>
<span data-ttu-id="18f15-114">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="18f15-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="18f15-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="18f15-115">This parameter is required.</span></span>

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

### <span data-ttu-id="18f15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18f15-116">-DefaultProfile</span></span>
<span data-ttu-id="18f15-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18f15-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18f15-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="18f15-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="18f15-119">Identificador da nova Confiuration do nome do host do gateway.</span><span class="sxs-lookup"><span data-stu-id="18f15-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="18f15-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="18f15-120">This parameter is optional.</span></span>
<span data-ttu-id="18f15-121">Se não for especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="18f15-121">If not specified will be generated.</span></span>

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

### <span data-ttu-id="18f15-122">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="18f15-122">-GatewayId</span></span>
<span data-ttu-id="18f15-123">Identificador do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="18f15-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="18f15-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="18f15-124">This parameter is required.</span></span>

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

### <span data-ttu-id="18f15-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="18f15-125">-Hostname</span></span>
<span data-ttu-id="18f15-126">Hostname.</span><span class="sxs-lookup"><span data-stu-id="18f15-126">Hostname.</span></span>
<span data-ttu-id="18f15-127">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="18f15-127">This parameter is required.</span></span>

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

### <span data-ttu-id="18f15-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="18f15-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="18f15-129">Sinalizador para impor NegotiateClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="18f15-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="18f15-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="18f15-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="18f15-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18f15-131">-Confirm</span></span>
<span data-ttu-id="18f15-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18f15-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18f15-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18f15-133">-WhatIf</span></span>
<span data-ttu-id="18f15-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18f15-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18f15-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18f15-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18f15-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f15-136">CommonParameters</span></span>
<span data-ttu-id="18f15-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18f15-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f15-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18f15-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f15-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18f15-139">INPUTS</span></span>

### <span data-ttu-id="18f15-140">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="18f15-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="18f15-141">System. String</span><span class="sxs-lookup"><span data-stu-id="18f15-141">System.String</span></span>

### <span data-ttu-id="18f15-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="18f15-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="18f15-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18f15-143">OUTPUTS</span></span>

### <span data-ttu-id="18f15-144">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="18f15-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="18f15-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18f15-145">NOTES</span></span>

## <span data-ttu-id="18f15-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18f15-146">RELATED LINKS</span></span>
