---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 2cde898622c870dc0598639addb1e8b30e438076
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598061"
---
# <span data-ttu-id="62f67-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="62f67-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="62f67-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62f67-102">SYNOPSIS</span></span>
<span data-ttu-id="62f67-103">Cria um novo contrato de credencial back-end.</span><span class="sxs-lookup"><span data-stu-id="62f67-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="62f67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62f67-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62f67-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62f67-105">DESCRIPTION</span></span>
<span data-ttu-id="62f67-106">Cria um novo contrato de credencial back-end.</span><span class="sxs-lookup"><span data-stu-id="62f67-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="62f67-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62f67-107">EXAMPLES</span></span>

### <span data-ttu-id="62f67-108">Criar uma In-Memory objeto de credenciais de back-end</span><span class="sxs-lookup"><span data-stu-id="62f67-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="62f67-109">Cria um contrato de credenciais de back-end</span><span class="sxs-lookup"><span data-stu-id="62f67-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="62f67-110">OS</span><span class="sxs-lookup"><span data-stu-id="62f67-110">PARAMETERS</span></span>

### <span data-ttu-id="62f67-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="62f67-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="62f67-112">Cabeçalho de autorização usado para o back-end.</span><span class="sxs-lookup"><span data-stu-id="62f67-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="62f67-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="62f67-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="62f67-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="62f67-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="62f67-115">Esquema de autorização usado para o back-end.</span><span class="sxs-lookup"><span data-stu-id="62f67-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="62f67-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="62f67-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="62f67-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="62f67-117">-CertificateThumbprint</span></span>
<span data-ttu-id="62f67-118">Impressões digitais de certificado de cliente.</span><span class="sxs-lookup"><span data-stu-id="62f67-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="62f67-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="62f67-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="62f67-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62f67-120">-DefaultProfile</span></span>
<span data-ttu-id="62f67-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62f67-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62f67-122">-Header</span><span class="sxs-lookup"><span data-stu-id="62f67-122">-Header</span></span>
<span data-ttu-id="62f67-123">Valores de parâmetro de cabeçalho aceitos pelo back-end.</span><span class="sxs-lookup"><span data-stu-id="62f67-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="62f67-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="62f67-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="62f67-125">-Consulta</span><span class="sxs-lookup"><span data-stu-id="62f67-125">-Query</span></span>
<span data-ttu-id="62f67-126">Valores de parâmetro de consulta aceitos pelo back-end.</span><span class="sxs-lookup"><span data-stu-id="62f67-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="62f67-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="62f67-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="62f67-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62f67-128">CommonParameters</span></span>
<span data-ttu-id="62f67-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62f67-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62f67-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62f67-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62f67-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62f67-131">INPUTS</span></span>

### <span data-ttu-id="62f67-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="62f67-132">None</span></span>

## <span data-ttu-id="62f67-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62f67-133">OUTPUTS</span></span>

### <span data-ttu-id="62f67-134">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="62f67-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="62f67-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62f67-135">NOTES</span></span>

## <span data-ttu-id="62f67-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62f67-136">RELATED LINKS</span></span>

[<span data-ttu-id="62f67-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="62f67-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="62f67-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="62f67-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="62f67-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="62f67-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="62f67-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="62f67-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="62f67-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="62f67-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
