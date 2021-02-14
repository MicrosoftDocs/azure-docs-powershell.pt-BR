---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 10c84654bb5d074ee9f668062d1fa7a18d92f8b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117044"
---
# <span data-ttu-id="713b1-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="713b1-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="713b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="713b1-102">SYNOPSIS</span></span>
<span data-ttu-id="713b1-103">Cria uma instância **do PsApiManagementHttpMessageDiagnostic,** que é uma configuração de diagnóstico de mensagem http do Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="713b1-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="713b1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="713b1-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="713b1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="713b1-105">DESCRIPTION</span></span>
<span data-ttu-id="713b1-106">O cmdlet **New-AzApiManagementHttpMessageDiagnostic** cria a configuração de diagnóstico de Mensagem Http.</span><span class="sxs-lookup"><span data-stu-id="713b1-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="713b1-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="713b1-107">EXAMPLES</span></span>

### <span data-ttu-id="713b1-108">Exemplo 1: Criar uma configuração básica de diagnóstico de mensagem http</span><span class="sxs-lookup"><span data-stu-id="713b1-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="713b1-109">Criar uma configuração de diagnóstico de mensagem http para log `Content-Type` e `User-Agent` cabeçalhos junto com 100 bytes de `body`</span><span class="sxs-lookup"><span data-stu-id="713b1-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="713b1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="713b1-110">PARAMETERS</span></span>

### <span data-ttu-id="713b1-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="713b1-111">-BodyBytesToLog</span></span>
<span data-ttu-id="713b1-112">Número de bytes do corpo de solicitação para log.</span><span class="sxs-lookup"><span data-stu-id="713b1-112">Number of request body bytes to log.</span></span> <span data-ttu-id="713b1-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="713b1-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="713b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="713b1-114">-DefaultProfile</span></span>
<span data-ttu-id="713b1-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="713b1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="713b1-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="713b1-116">-HeadersToLog</span></span>
<span data-ttu-id="713b1-117">A matriz de headers para log.</span><span class="sxs-lookup"><span data-stu-id="713b1-117">The array of headers to log.</span></span> <span data-ttu-id="713b1-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="713b1-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="713b1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="713b1-119">CommonParameters</span></span>
<span data-ttu-id="713b1-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="713b1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="713b1-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="713b1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="713b1-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="713b1-122">INPUTS</span></span>

### <span data-ttu-id="713b1-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="713b1-123">None</span></span>

## <span data-ttu-id="713b1-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="713b1-124">OUTPUTS</span></span>

### <span data-ttu-id="713b1-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="713b1-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="713b1-126">Notas</span><span class="sxs-lookup"><span data-stu-id="713b1-126">NOTES</span></span>

## <span data-ttu-id="713b1-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="713b1-127">RELATED LINKS</span></span>

[<span data-ttu-id="713b1-128">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="713b1-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="713b1-129">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="713b1-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)