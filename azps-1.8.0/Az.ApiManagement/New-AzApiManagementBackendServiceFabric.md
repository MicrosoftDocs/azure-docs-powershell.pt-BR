---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: 193f8f64abee3514d94a0f825beb7190c8ea7fa6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595640"
---
# <span data-ttu-id="20a0e-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="20a0e-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="20a0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="20a0e-103">Cria um objeto de `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="20a0e-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="20a0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20a0e-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20a0e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20a0e-105">DESCRIPTION</span></span>

<span data-ttu-id="20a0e-106">O cmdlet **New-AzApiManagementBackendServiceFabric** cria um objeto de `PsApiManagementServiceFabric` para ser usado em cmdlet **New-AzApiManagementBackend** e **set-AzApiManagementBackend**.</span><span class="sxs-lookup"><span data-stu-id="20a0e-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="20a0e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20a0e-107">EXAMPLES</span></span>

### <span data-ttu-id="20a0e-108">Exemplo 1: criar um objeto de In-Memory do serviço de back-Fabric</span><span class="sxs-lookup"><span data-stu-id="20a0e-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="20a0e-109">Cria um contrato de malha do serviço back-end</span><span class="sxs-lookup"><span data-stu-id="20a0e-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="20a0e-110">OS</span><span class="sxs-lookup"><span data-stu-id="20a0e-110">PARAMETERS</span></span>

### <span data-ttu-id="20a0e-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="20a0e-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="20a0e-112">Impressão digital do certificado do cliente para o ponto de extremidade de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="20a0e-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="20a0e-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="20a0e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="20a0e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a0e-114">-DefaultProfile</span></span>
<span data-ttu-id="20a0e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20a0e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20a0e-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="20a0e-116">-ManagementEndpoint</span></span>
<span data-ttu-id="20a0e-117">Pontos de extremidade de gerenciamento de cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="20a0e-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="20a0e-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="20a0e-118">This parameter is required.</span></span>

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

### <span data-ttu-id="20a0e-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="20a0e-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="20a0e-120">Número máximo de tentativas ao resolver uma partição do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="20a0e-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="20a0e-121">Esse parâmetro é opcional e o valor padrão é 5.</span><span class="sxs-lookup"><span data-stu-id="20a0e-121">This parameter is optional and default value is 5.</span></span>

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

### <span data-ttu-id="20a0e-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="20a0e-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="20a0e-123">Impressão digital de certificados o serviço de gerenciamento de cluster usa para comunicação TLS. Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="20a0e-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

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

### <span data-ttu-id="20a0e-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="20a0e-124">-ServerX509Name</span></span>
<span data-ttu-id="20a0e-125">Coleção de nomes de certificados X509 do servidor.</span><span class="sxs-lookup"><span data-stu-id="20a0e-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="20a0e-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="20a0e-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="20a0e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a0e-127">CommonParameters</span></span>
<span data-ttu-id="20a0e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a0e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a0e-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20a0e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a0e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20a0e-130">INPUTS</span></span>

### <span data-ttu-id="20a0e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="20a0e-131">System.String</span></span>

## <span data-ttu-id="20a0e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20a0e-132">OUTPUTS</span></span>

### <span data-ttu-id="20a0e-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="20a0e-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="20a0e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20a0e-134">NOTES</span></span>

## <span data-ttu-id="20a0e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20a0e-135">RELATED LINKS</span></span>

[<span data-ttu-id="20a0e-136">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="20a0e-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="20a0e-137">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="20a0e-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="20a0e-138">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="20a0e-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="20a0e-139">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="20a0e-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="20a0e-140">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="20a0e-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
