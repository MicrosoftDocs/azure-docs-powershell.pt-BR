---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 0d865e2b9e1459f326367a499e30bc37467628cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887243"
---
# <span data-ttu-id="a4be3-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a4be3-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="a4be3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4be3-102">SYNOPSIS</span></span>
<span data-ttu-id="a4be3-103">Cria um novo contrato de Credencial de Back-end.</span><span class="sxs-lookup"><span data-stu-id="a4be3-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="a4be3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a4be3-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4be3-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a4be3-105">DESCRIPTION</span></span>
<span data-ttu-id="a4be3-106">Cria um novo contrato de Credencial de Back-end.</span><span class="sxs-lookup"><span data-stu-id="a4be3-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="a4be3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4be3-107">EXAMPLES</span></span>

### <span data-ttu-id="a4be3-108">Exemplo 1: Criar um objeto Back-end Credentials In-Memory.</span><span class="sxs-lookup"><span data-stu-id="a4be3-108">Example 1: Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="a4be3-109">Cria um contrato de credenciais back-end</span><span class="sxs-lookup"><span data-stu-id="a4be3-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="a4be3-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a4be3-110">PARAMETERS</span></span>

### <span data-ttu-id="a4be3-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="a4be3-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="a4be3-112">Header de Autorização usado para o Backend.</span><span class="sxs-lookup"><span data-stu-id="a4be3-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="a4be3-113">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a4be3-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="a4be3-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="a4be3-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="a4be3-115">Esquema de Autorização usado para o Backend.</span><span class="sxs-lookup"><span data-stu-id="a4be3-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="a4be3-116">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a4be3-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="a4be3-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="a4be3-117">-CertificateThumbprint</span></span>
<span data-ttu-id="a4be3-118">Thumbprints de certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="a4be3-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="a4be3-119">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a4be3-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="a4be3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4be3-120">-DefaultProfile</span></span>
<span data-ttu-id="a4be3-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a4be3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4be3-122">-Header</span><span class="sxs-lookup"><span data-stu-id="a4be3-122">-Header</span></span>
<span data-ttu-id="a4be3-123">Valores de parâmetro de header aceitos por Backend.</span><span class="sxs-lookup"><span data-stu-id="a4be3-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="a4be3-124">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a4be3-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="a4be3-125">-Query</span><span class="sxs-lookup"><span data-stu-id="a4be3-125">-Query</span></span>
<span data-ttu-id="a4be3-126">Valores de parâmetro de consulta aceitos por Backend.</span><span class="sxs-lookup"><span data-stu-id="a4be3-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="a4be3-127">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a4be3-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="a4be3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4be3-128">CommonParameters</span></span>
<span data-ttu-id="a4be3-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4be3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4be3-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4be3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4be3-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4be3-131">INPUTS</span></span>

### <span data-ttu-id="a4be3-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a4be3-132">None</span></span>

## <span data-ttu-id="a4be3-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a4be3-133">OUTPUTS</span></span>

### <span data-ttu-id="a4be3-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a4be3-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="a4be3-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="a4be3-135">NOTES</span></span>

## <span data-ttu-id="a4be3-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4be3-136">RELATED LINKS</span></span>

[<span data-ttu-id="a4be3-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a4be3-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="a4be3-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a4be3-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="a4be3-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a4be3-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="a4be3-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a4be3-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="a4be3-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a4be3-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
