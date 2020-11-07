---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/resume-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
ms.openlocfilehash: 3614c62af825b109b224d231d89dda315a7e2616
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942050"
---
# <span data-ttu-id="1b3cf-101">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1b3cf-101">Resume-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="1b3cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b3cf-102">SYNOPSIS</span></span>
<span data-ttu-id="1b3cf-103">Retoma uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="1b3cf-103">Resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="1b3cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b3cf-104">SYNTAX</span></span>

```
Resume-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b3cf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b3cf-105">DESCRIPTION</span></span>
<span data-ttu-id="1b3cf-106">O cmdlet Resume-AzAnalysisServicesServer retoma uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="1b3cf-106">The Resume-AzAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="1b3cf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b3cf-107">EXAMPLES</span></span>

### <span data-ttu-id="1b3cf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1b3cf-108">Example 1</span></span>
```
PS C:\> Resume-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="1b3cf-109">Esse comando retomará um servidor pausado chamado TestServer no de teste do meu nome do o-botão</span><span class="sxs-lookup"><span data-stu-id="1b3cf-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="1b3cf-110">OS</span><span class="sxs-lookup"><span data-stu-id="1b3cf-110">PARAMETERS</span></span>

### <span data-ttu-id="1b3cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b3cf-111">-DefaultProfile</span></span>
<span data-ttu-id="1b3cf-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b3cf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b3cf-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b3cf-113">-Name</span></span>
<span data-ttu-id="1b3cf-114">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="1b3cf-114">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b3cf-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b3cf-115">-PassThru</span></span>
<span data-ttu-id="1b3cf-116">Retornará os detalhes do servidor excluído se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="1b3cf-116">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b3cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="1b3cf-118">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="1b3cf-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b3cf-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1b3cf-119">-Confirm</span></span>
<span data-ttu-id="1b3cf-120">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="1b3cf-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3cf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b3cf-121">-WhatIf</span></span>
<span data-ttu-id="1b3cf-122">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="1b3cf-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3cf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b3cf-123">CommonParameters</span></span>
<span data-ttu-id="1b3cf-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b3cf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b3cf-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b3cf-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b3cf-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b3cf-126">INPUTS</span></span>

### <span data-ttu-id="1b3cf-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1b3cf-127">System.String</span></span>

## <span data-ttu-id="1b3cf-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b3cf-128">OUTPUTS</span></span>

### <span data-ttu-id="1b3cf-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1b3cf-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="1b3cf-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b3cf-130">NOTES</span></span>
<span data-ttu-id="1b3cf-131">Alias: Resume-AzAs</span><span class="sxs-lookup"><span data-stu-id="1b3cf-131">Alias: Resume-AzAs</span></span>

## <span data-ttu-id="1b3cf-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b3cf-132">RELATED LINKS</span></span>

[<span data-ttu-id="1b3cf-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1b3cf-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="1b3cf-134">Suspender-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1b3cf-134">Suspend-AzAnalysisServicesServer</span></span>](./Suspend-AzAnalysisServicesServer.md)
