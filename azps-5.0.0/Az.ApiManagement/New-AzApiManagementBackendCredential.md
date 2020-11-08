---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 069bf57b62d6834a1509adb551d15ce5082b2dc3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116284"
---
# <span data-ttu-id="b36cf-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b36cf-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="b36cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b36cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b36cf-103">Cria um novo contrato de credencial back-end.</span><span class="sxs-lookup"><span data-stu-id="b36cf-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="b36cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b36cf-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b36cf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b36cf-105">DESCRIPTION</span></span>
<span data-ttu-id="b36cf-106">Cria um novo contrato de credencial back-end.</span><span class="sxs-lookup"><span data-stu-id="b36cf-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="b36cf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b36cf-107">EXAMPLES</span></span>

### <span data-ttu-id="b36cf-108">Exemplo 1: criar um objeto In-Memory de credenciais de back-end</span><span class="sxs-lookup"><span data-stu-id="b36cf-108">Example 1: Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="b36cf-109">Cria um contrato de credenciais de back-end</span><span class="sxs-lookup"><span data-stu-id="b36cf-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="b36cf-110">OS</span><span class="sxs-lookup"><span data-stu-id="b36cf-110">PARAMETERS</span></span>

### <span data-ttu-id="b36cf-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="b36cf-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="b36cf-112">Cabeçalho de autorização usado para o back-end.</span><span class="sxs-lookup"><span data-stu-id="b36cf-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="b36cf-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b36cf-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="b36cf-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="b36cf-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="b36cf-115">Esquema de autorização usado para o back-end.</span><span class="sxs-lookup"><span data-stu-id="b36cf-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="b36cf-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b36cf-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="b36cf-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b36cf-117">-CertificateThumbprint</span></span>
<span data-ttu-id="b36cf-118">Impressões digitais de certificado de cliente.</span><span class="sxs-lookup"><span data-stu-id="b36cf-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="b36cf-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b36cf-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="b36cf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b36cf-120">-DefaultProfile</span></span>
<span data-ttu-id="b36cf-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b36cf-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b36cf-122">-Header</span><span class="sxs-lookup"><span data-stu-id="b36cf-122">-Header</span></span>
<span data-ttu-id="b36cf-123">Valores de parâmetro de cabeçalho aceitos pelo back-end.</span><span class="sxs-lookup"><span data-stu-id="b36cf-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="b36cf-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b36cf-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="b36cf-125">-Consulta</span><span class="sxs-lookup"><span data-stu-id="b36cf-125">-Query</span></span>
<span data-ttu-id="b36cf-126">Valores de parâmetro de consulta aceitos pelo back-end.</span><span class="sxs-lookup"><span data-stu-id="b36cf-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="b36cf-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b36cf-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="b36cf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b36cf-128">CommonParameters</span></span>
<span data-ttu-id="b36cf-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b36cf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b36cf-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b36cf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b36cf-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b36cf-131">INPUTS</span></span>

### <span data-ttu-id="b36cf-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b36cf-132">None</span></span>

## <span data-ttu-id="b36cf-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b36cf-133">OUTPUTS</span></span>

### <span data-ttu-id="b36cf-134">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b36cf-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="b36cf-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b36cf-135">NOTES</span></span>

## <span data-ttu-id="b36cf-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b36cf-136">RELATED LINKS</span></span>

[<span data-ttu-id="b36cf-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b36cf-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="b36cf-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b36cf-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="b36cf-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b36cf-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="b36cf-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b36cf-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="b36cf-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b36cf-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
