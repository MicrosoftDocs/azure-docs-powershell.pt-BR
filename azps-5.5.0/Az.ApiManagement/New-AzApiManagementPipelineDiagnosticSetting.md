---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: 7e6f6515b24a7cefabd40a6fdfaedfda430f69d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116655"
---
# <span data-ttu-id="0ab54-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="0ab54-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="0ab54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ab54-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab54-103">Crie configurações de Diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="0ab54-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="0ab54-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ab54-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ab54-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ab54-105">DESCRIPTION</span></span>
<span data-ttu-id="0ab54-106">O cmdlet **New-AzApiManagement DimensionalLineDiagnosticSetting** cria as configurações de Diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="0ab54-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="0ab54-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0ab54-107">EXAMPLES</span></span>

### <span data-ttu-id="0ab54-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0ab54-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="0ab54-109">Crie um diagnóstico de pipeline a ser usado em FrontEnd ou Backend na Entidade de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="0ab54-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="0ab54-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ab54-110">PARAMETERS</span></span>

### <span data-ttu-id="0ab54-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab54-111">-DefaultProfile</span></span>
<span data-ttu-id="0ab54-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0ab54-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ab54-113">-Solicitação</span><span class="sxs-lookup"><span data-stu-id="0ab54-113">-Request</span></span>
<span data-ttu-id="0ab54-114">Configuração de diagnóstico para Solicitação.</span><span class="sxs-lookup"><span data-stu-id="0ab54-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="0ab54-115">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0ab54-115">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab54-116">-Resposta</span><span class="sxs-lookup"><span data-stu-id="0ab54-116">-Response</span></span>
<span data-ttu-id="0ab54-117">Configuração de diagnóstico para Resposta.</span><span class="sxs-lookup"><span data-stu-id="0ab54-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="0ab54-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0ab54-118">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab54-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab54-119">CommonParameters</span></span>
<span data-ttu-id="0ab54-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab54-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab54-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ab54-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab54-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="0ab54-122">INPUTS</span></span>

### <span data-ttu-id="0ab54-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0ab54-123">None</span></span>

## <span data-ttu-id="0ab54-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="0ab54-124">OUTPUTS</span></span>

### <span data-ttu-id="0ab54-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="0ab54-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="0ab54-126">Notas</span><span class="sxs-lookup"><span data-stu-id="0ab54-126">NOTES</span></span>

## <span data-ttu-id="0ab54-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ab54-127">RELATED LINKS</span></span>

[<span data-ttu-id="0ab54-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0ab54-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="0ab54-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0ab54-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="0ab54-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0ab54-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="0ab54-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0ab54-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


