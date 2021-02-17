---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 3d9a462a034c5c1e65ff6b22fe92b14421582392
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401259"
---
# <span data-ttu-id="2505f-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="2505f-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="2505f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2505f-102">SYNOPSIS</span></span>
<span data-ttu-id="2505f-103">Cria um novo contrato de Credenciais de Backend.</span><span class="sxs-lookup"><span data-stu-id="2505f-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="2505f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2505f-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2505f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2505f-105">DESCRIPTION</span></span>
<span data-ttu-id="2505f-106">Cria um novo contrato de Credencial back-end.</span><span class="sxs-lookup"><span data-stu-id="2505f-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="2505f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2505f-107">EXAMPLES</span></span>

### <span data-ttu-id="2505f-108">Criar um Backend Credentials In-Memory Objeto</span><span class="sxs-lookup"><span data-stu-id="2505f-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="2505f-109">Cria um Contrato de Credenciais de Backend</span><span class="sxs-lookup"><span data-stu-id="2505f-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="2505f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2505f-110">PARAMETERS</span></span>

### <span data-ttu-id="2505f-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="2505f-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="2505f-112">Header de Autorização usado para o Backend.</span><span class="sxs-lookup"><span data-stu-id="2505f-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="2505f-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="2505f-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="2505f-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="2505f-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="2505f-115">Esquema de Autorização usado para o Backend.</span><span class="sxs-lookup"><span data-stu-id="2505f-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="2505f-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="2505f-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="2505f-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="2505f-117">-CertificateThumbprint</span></span>
<span data-ttu-id="2505f-118">Miniaturas de certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="2505f-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="2505f-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="2505f-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="2505f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2505f-120">-DefaultProfile</span></span>
<span data-ttu-id="2505f-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2505f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2505f-122">-Header</span><span class="sxs-lookup"><span data-stu-id="2505f-122">-Header</span></span>
<span data-ttu-id="2505f-123">Valores de parâmetro de header aceitos por Backend.</span><span class="sxs-lookup"><span data-stu-id="2505f-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="2505f-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="2505f-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="2505f-125">-Consulta</span><span class="sxs-lookup"><span data-stu-id="2505f-125">-Query</span></span>
<span data-ttu-id="2505f-126">Valores de parâmetro de consulta aceitos por Backend.</span><span class="sxs-lookup"><span data-stu-id="2505f-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="2505f-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="2505f-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="2505f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2505f-128">CommonParameters</span></span>
<span data-ttu-id="2505f-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2505f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2505f-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2505f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2505f-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="2505f-131">INPUTS</span></span>

### <span data-ttu-id="2505f-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2505f-132">None</span></span>

## <span data-ttu-id="2505f-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="2505f-133">OUTPUTS</span></span>

### <span data-ttu-id="2505f-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="2505f-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="2505f-135">Notas</span><span class="sxs-lookup"><span data-stu-id="2505f-135">NOTES</span></span>

## <span data-ttu-id="2505f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2505f-136">RELATED LINKS</span></span>

[<span data-ttu-id="2505f-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2505f-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="2505f-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2505f-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="2505f-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="2505f-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="2505f-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2505f-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="2505f-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2505f-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
