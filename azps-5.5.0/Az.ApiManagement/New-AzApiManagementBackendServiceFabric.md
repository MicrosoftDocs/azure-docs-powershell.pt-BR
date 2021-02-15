---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: 352e40aa64adf5eea98950ac9271f0237e634ab6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118054"
---
# <span data-ttu-id="b7214-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7214-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="b7214-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7214-102">SYNOPSIS</span></span>
<span data-ttu-id="b7214-103">Cria um objeto de `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="b7214-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="b7214-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7214-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7214-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7214-105">DESCRIPTION</span></span>

<span data-ttu-id="b7214-106">O cmdlet **New-AzApiManagementBackendServiceFabric** cria um objeto de ser usado no `PsApiManagementServiceFabric` cmdlet **New-AzApiManagementBackend** e **Set-AzApiManagementBackend.**</span><span class="sxs-lookup"><span data-stu-id="b7214-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="b7214-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b7214-107">EXAMPLES</span></span>

### <span data-ttu-id="b7214-108">Exemplo 1: Criar um objeto Backend Service Fabric In-Memory</span><span class="sxs-lookup"><span data-stu-id="b7214-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="b7214-109">Cria um Contrato de Malha de Serviço back-end</span><span class="sxs-lookup"><span data-stu-id="b7214-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="b7214-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7214-110">PARAMETERS</span></span>

### <span data-ttu-id="b7214-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b7214-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="b7214-112">Thumbprint de certificado do cliente para o ponto de extremidade de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="b7214-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="b7214-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b7214-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b7214-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7214-114">-DefaultProfile</span></span>
<span data-ttu-id="b7214-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7214-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7214-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7214-116">-ManagementEndpoint</span></span>
<span data-ttu-id="b7214-117">Pontos de extremidade de gerenciamento de cluster de malha de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7214-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="b7214-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b7214-118">This parameter is required.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7214-119">-MaxPartitionResolutionVolry</span><span class="sxs-lookup"><span data-stu-id="b7214-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="b7214-120">Número máximo de recuperações ao resolver uma partição de Malha de Serviço.</span><span class="sxs-lookup"><span data-stu-id="b7214-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="b7214-121">Este parâmetro é opcional e o valor padrão é 5.</span><span class="sxs-lookup"><span data-stu-id="b7214-121">This parameter is optional and default value is 5.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7214-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b7214-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="b7214-123">Impressão digital de certificados que o serviço de gerenciamento de cluster usa para comunicação tls. Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b7214-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7214-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="b7214-124">-ServerX509Name</span></span>
<span data-ttu-id="b7214-125">Server X509 Certificate Names Collection.</span><span class="sxs-lookup"><span data-stu-id="b7214-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="b7214-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b7214-126">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7214-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7214-127">CommonParameters</span></span>
<span data-ttu-id="b7214-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7214-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7214-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7214-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7214-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="b7214-130">INPUTS</span></span>

### <span data-ttu-id="b7214-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b7214-131">System.String</span></span>

## <span data-ttu-id="b7214-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="b7214-132">OUTPUTS</span></span>

### <span data-ttu-id="b7214-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7214-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="b7214-134">Notas</span><span class="sxs-lookup"><span data-stu-id="b7214-134">NOTES</span></span>

## <span data-ttu-id="b7214-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7214-135">RELATED LINKS</span></span>

[<span data-ttu-id="b7214-136">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b7214-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="b7214-137">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b7214-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="b7214-138">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b7214-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="b7214-139">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b7214-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="b7214-140">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b7214-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
