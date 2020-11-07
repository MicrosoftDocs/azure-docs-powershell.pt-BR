---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 069bf57b62d6834a1509adb551d15ce5082b2dc3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955834"
---
# <span data-ttu-id="b1a8f-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b1a8f-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="b1a8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a8f-103">Cria um novo contrato de credencial back-end.</span><span class="sxs-lookup"><span data-stu-id="b1a8f-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="b1a8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1a8f-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1a8f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1a8f-105">DESCRIPTION</span></span>
<span data-ttu-id="b1a8f-106">Cria um novo contrato de credencial back-end.</span><span class="sxs-lookup"><span data-stu-id="b1a8f-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="b1a8f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1a8f-107">EXAMPLES</span></span>

### <span data-ttu-id="b1a8f-108">Exemplo 1: criar um objeto In-Memory de credenciais de back-end</span><span class="sxs-lookup"><span data-stu-id="b1a8f-108">Example 1: Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="b1a8f-109">Cria um contrato de credenciais de back-end</span><span class="sxs-lookup"><span data-stu-id="b1a8f-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="b1a8f-110">OS</span><span class="sxs-lookup"><span data-stu-id="b1a8f-110">PARAMETERS</span></span>

### <span data-ttu-id="b1a8f-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="b1a8f-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="b1a8f-112">Cabeçalho de autorização usado para o back-end.</span><span class="sxs-lookup"><span data-stu-id="b1a8f-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="b1a8f-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b1a8f-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a8f-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="b1a8f-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="b1a8f-115">Esquema de autorização usado para o back-end.</span><span class="sxs-lookup"><span data-stu-id="b1a8f-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="b1a8f-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b1a8f-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a8f-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b1a8f-117">-CertificateThumbprint</span></span>
<span data-ttu-id="b1a8f-118">Impressões digitais de certificado de cliente.</span><span class="sxs-lookup"><span data-stu-id="b1a8f-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="b1a8f-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b1a8f-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="b1a8f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a8f-120">-DefaultProfile</span></span>
<span data-ttu-id="b1a8f-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1a8f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1a8f-122">-Header</span><span class="sxs-lookup"><span data-stu-id="b1a8f-122">-Header</span></span>
<span data-ttu-id="b1a8f-123">Valores de parâmetro de cabeçalho aceitos pelo back-end.</span><span class="sxs-lookup"><span data-stu-id="b1a8f-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="b1a8f-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b1a8f-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="b1a8f-125">-Consulta</span><span class="sxs-lookup"><span data-stu-id="b1a8f-125">-Query</span></span>
<span data-ttu-id="b1a8f-126">Valores de parâmetro de consulta aceitos pelo back-end.</span><span class="sxs-lookup"><span data-stu-id="b1a8f-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="b1a8f-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b1a8f-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="b1a8f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a8f-128">CommonParameters</span></span>
<span data-ttu-id="b1a8f-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1a8f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a8f-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1a8f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a8f-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1a8f-131">INPUTS</span></span>

### <span data-ttu-id="b1a8f-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b1a8f-132">None</span></span>

## <span data-ttu-id="b1a8f-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1a8f-133">OUTPUTS</span></span>

### <span data-ttu-id="b1a8f-134">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b1a8f-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="b1a8f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1a8f-135">NOTES</span></span>

## <span data-ttu-id="b1a8f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1a8f-136">RELATED LINKS</span></span>

[<span data-ttu-id="b1a8f-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b1a8f-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="b1a8f-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b1a8f-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="b1a8f-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b1a8f-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="b1a8f-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b1a8f-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="b1a8f-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b1a8f-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
