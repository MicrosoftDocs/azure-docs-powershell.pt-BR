---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: ded8b44940c227477f6ad3dfdd7d4b673161fca1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399440"
---
# <span data-ttu-id="862eb-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="862eb-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="862eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="862eb-102">SYNOPSIS</span></span>
<span data-ttu-id="862eb-103">Cria um novo contrato de Credencial back-end.</span><span class="sxs-lookup"><span data-stu-id="862eb-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="862eb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="862eb-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="862eb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="862eb-105">DESCRIPTION</span></span>
<span data-ttu-id="862eb-106">Cria um novo contrato de Credenciais de Backend.</span><span class="sxs-lookup"><span data-stu-id="862eb-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="862eb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="862eb-107">EXAMPLES</span></span>

### <span data-ttu-id="862eb-108">Criar um Backend Credentials In-Memory Object</span><span class="sxs-lookup"><span data-stu-id="862eb-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="862eb-109">Cria um Contrato de Credenciais de Backend</span><span class="sxs-lookup"><span data-stu-id="862eb-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="862eb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="862eb-110">PARAMETERS</span></span>

### <span data-ttu-id="862eb-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="862eb-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="862eb-112">Header de Autorização usado para o Backend.</span><span class="sxs-lookup"><span data-stu-id="862eb-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="862eb-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="862eb-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="862eb-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="862eb-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="862eb-115">Esquema de Autorização usado para o Backend.</span><span class="sxs-lookup"><span data-stu-id="862eb-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="862eb-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="862eb-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="862eb-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="862eb-117">-CertificateThumbprint</span></span>
<span data-ttu-id="862eb-118">Miniaturas de certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="862eb-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="862eb-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="862eb-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="862eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="862eb-120">-DefaultProfile</span></span>
<span data-ttu-id="862eb-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="862eb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="862eb-122">-Header</span><span class="sxs-lookup"><span data-stu-id="862eb-122">-Header</span></span>
<span data-ttu-id="862eb-123">Valores de parâmetro de header aceitos por Backend.</span><span class="sxs-lookup"><span data-stu-id="862eb-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="862eb-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="862eb-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="862eb-125">-Consulta</span><span class="sxs-lookup"><span data-stu-id="862eb-125">-Query</span></span>
<span data-ttu-id="862eb-126">Valores de parâmetro de consulta aceitos por Backend.</span><span class="sxs-lookup"><span data-stu-id="862eb-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="862eb-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="862eb-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="862eb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="862eb-128">CommonParameters</span></span>
<span data-ttu-id="862eb-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="862eb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="862eb-130">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="862eb-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="862eb-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="862eb-131">INPUTS</span></span>

### <span data-ttu-id="862eb-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="862eb-132">None</span></span>

## <span data-ttu-id="862eb-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="862eb-133">OUTPUTS</span></span>

### <span data-ttu-id="862eb-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="862eb-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="862eb-135">Notas</span><span class="sxs-lookup"><span data-stu-id="862eb-135">NOTES</span></span>

## <span data-ttu-id="862eb-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="862eb-136">RELATED LINKS</span></span>

[<span data-ttu-id="862eb-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="862eb-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="862eb-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="862eb-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="862eb-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="862eb-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="862eb-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="862eb-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="862eb-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="862eb-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
