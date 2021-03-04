---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 3475778104655e6b27061edf08ced376f192ea34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890028"
---
# <span data-ttu-id="8efad-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8efad-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="8efad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8efad-102">SYNOPSIS</span></span>
<span data-ttu-id="8efad-103">Cria uma instância **de PsApiManagementHttpMessageDiagnostic** que é uma configuração de diagnóstico de Mensagem Http do Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="8efad-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="8efad-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8efad-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8efad-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8efad-105">DESCRIPTION</span></span>
<span data-ttu-id="8efad-106">O cmdlet **New-AzApiManagementHttpMessageDiagnostic** cria a configuração de diagnóstico de Mensagem Http.</span><span class="sxs-lookup"><span data-stu-id="8efad-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="8efad-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8efad-107">EXAMPLES</span></span>

### <span data-ttu-id="8efad-108">Exemplo 1: Criar uma configuração básica de diagnóstico de mensagem http</span><span class="sxs-lookup"><span data-stu-id="8efad-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="8efad-109">Criar uma configuração de diagnóstico de mensagem http para log `Content-Type` `User-Agent` e cabeçalhos, juntamente com 100 bytes de `body`</span><span class="sxs-lookup"><span data-stu-id="8efad-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="8efad-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8efad-110">PARAMETERS</span></span>

### <span data-ttu-id="8efad-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="8efad-111">-BodyBytesToLog</span></span>
<span data-ttu-id="8efad-112">Número de bytes do corpo da solicitação para fazer o log.</span><span class="sxs-lookup"><span data-stu-id="8efad-112">Number of request body bytes to log.</span></span> <span data-ttu-id="8efad-113">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8efad-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="8efad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8efad-114">-DefaultProfile</span></span>
<span data-ttu-id="8efad-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8efad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8efad-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="8efad-116">-HeadersToLog</span></span>
<span data-ttu-id="8efad-117">A matriz de headers a ser log.</span><span class="sxs-lookup"><span data-stu-id="8efad-117">The array of headers to log.</span></span> <span data-ttu-id="8efad-118">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8efad-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="8efad-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8efad-119">CommonParameters</span></span>
<span data-ttu-id="8efad-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8efad-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8efad-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8efad-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8efad-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8efad-122">INPUTS</span></span>

### <span data-ttu-id="8efad-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8efad-123">None</span></span>

## <span data-ttu-id="8efad-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8efad-124">OUTPUTS</span></span>

### <span data-ttu-id="8efad-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8efad-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="8efad-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="8efad-126">NOTES</span></span>

## <span data-ttu-id="8efad-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8efad-127">RELATED LINKS</span></span>

[<span data-ttu-id="8efad-128">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8efad-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8efad-129">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="8efad-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)