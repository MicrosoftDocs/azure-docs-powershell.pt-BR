---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: e68449a84bb64454291434bded40ed2e494fdab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888767"
---
# <span data-ttu-id="6957d-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="6957d-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="6957d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6957d-102">SYNOPSIS</span></span>
<span data-ttu-id="6957d-103">Crie configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="6957d-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="6957d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6957d-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6957d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6957d-105">DESCRIPTION</span></span>
<span data-ttu-id="6957d-106">O cmdlet **New-AzApiManagementPipelineDiagnosticSetting** cria as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="6957d-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="6957d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6957d-107">EXAMPLES</span></span>

### <span data-ttu-id="6957d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6957d-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="6957d-109">Crie um diagnóstico de pipeline a ser usado em FrontEnd ou Backend na Entidade de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="6957d-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="6957d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6957d-110">PARAMETERS</span></span>

### <span data-ttu-id="6957d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6957d-111">-DefaultProfile</span></span>
<span data-ttu-id="6957d-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6957d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6957d-113">-Request</span><span class="sxs-lookup"><span data-stu-id="6957d-113">-Request</span></span>
<span data-ttu-id="6957d-114">Configuração de diagnóstico para Solicitação.</span><span class="sxs-lookup"><span data-stu-id="6957d-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="6957d-115">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="6957d-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="6957d-116">-Response</span><span class="sxs-lookup"><span data-stu-id="6957d-116">-Response</span></span>
<span data-ttu-id="6957d-117">Configuração de diagnóstico para Resposta.</span><span class="sxs-lookup"><span data-stu-id="6957d-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="6957d-118">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="6957d-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="6957d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6957d-119">CommonParameters</span></span>
<span data-ttu-id="6957d-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6957d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6957d-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6957d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6957d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6957d-122">INPUTS</span></span>

### <span data-ttu-id="6957d-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6957d-123">None</span></span>

## <span data-ttu-id="6957d-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6957d-124">OUTPUTS</span></span>

### <span data-ttu-id="6957d-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="6957d-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="6957d-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="6957d-126">NOTES</span></span>

## <span data-ttu-id="6957d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6957d-127">RELATED LINKS</span></span>

[<span data-ttu-id="6957d-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6957d-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="6957d-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6957d-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="6957d-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6957d-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="6957d-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6957d-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


