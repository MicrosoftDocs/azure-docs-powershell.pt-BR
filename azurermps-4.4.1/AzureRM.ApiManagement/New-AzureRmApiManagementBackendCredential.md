---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 58f80b6ff1742bfc6360844648d6ad18d12d8389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431234"
---
# <span data-ttu-id="7f68c-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="7f68c-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="7f68c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f68c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f68c-103">Cria um novo contrato de credencial back-end.</span><span class="sxs-lookup"><span data-stu-id="7f68c-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f68c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f68c-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f68c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f68c-105">DESCRIPTION</span></span>
<span data-ttu-id="7f68c-106">Cria um novo contrato de credencial back-end.</span><span class="sxs-lookup"><span data-stu-id="7f68c-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="7f68c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f68c-107">EXAMPLES</span></span>

### <span data-ttu-id="7f68c-108">Criar uma In-Memory objeto de credenciais de back-end</span><span class="sxs-lookup"><span data-stu-id="7f68c-108">Create a Backend Credentials In-Memory Object</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="7f68c-109">Cria um contrato de credenciais de back-end</span><span class="sxs-lookup"><span data-stu-id="7f68c-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="7f68c-110">OS</span><span class="sxs-lookup"><span data-stu-id="7f68c-110">PARAMETERS</span></span>

### <span data-ttu-id="7f68c-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="7f68c-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="7f68c-112">Cabeçalho de autorização usado para o back-end.</span><span class="sxs-lookup"><span data-stu-id="7f68c-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="7f68c-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7f68c-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="7f68c-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="7f68c-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="7f68c-115">Esquema de autorização usado para o back-end.</span><span class="sxs-lookup"><span data-stu-id="7f68c-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="7f68c-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7f68c-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="7f68c-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="7f68c-117">-CertificateThumbprint</span></span>
<span data-ttu-id="7f68c-118">Impressões digitais de certificado de cliente.</span><span class="sxs-lookup"><span data-stu-id="7f68c-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="7f68c-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7f68c-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="7f68c-120">-Header</span><span class="sxs-lookup"><span data-stu-id="7f68c-120">-Header</span></span>
<span data-ttu-id="7f68c-121">Valores de parâmetro de cabeçalho aceitos pelo back-end.</span><span class="sxs-lookup"><span data-stu-id="7f68c-121">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="7f68c-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7f68c-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="7f68c-123">-Consulta</span><span class="sxs-lookup"><span data-stu-id="7f68c-123">-Query</span></span>
<span data-ttu-id="7f68c-124">Valores de parâmetro de consulta aceitos pelo back-end.</span><span class="sxs-lookup"><span data-stu-id="7f68c-124">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="7f68c-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7f68c-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="7f68c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f68c-126">-DefaultProfile</span></span>
<span data-ttu-id="7f68c-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f68c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f68c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f68c-128">CommonParameters</span></span>
<span data-ttu-id="7f68c-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f68c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f68c-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f68c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f68c-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f68c-131">INPUTS</span></span>

## <span data-ttu-id="7f68c-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f68c-132">OUTPUTS</span></span>

### <span data-ttu-id="7f68c-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="7f68c-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="7f68c-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f68c-134">NOTES</span></span>

## <span data-ttu-id="7f68c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f68c-135">RELATED LINKS</span></span>

[<span data-ttu-id="7f68c-136">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7f68c-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="7f68c-137">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7f68c-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="7f68c-138">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="7f68c-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="7f68c-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7f68c-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="7f68c-140">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7f68c-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
