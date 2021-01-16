---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/suspend-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
ms.openlocfilehash: 135403f8654b46a55dae9fafaacc0e01508579c3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432778"
---
# <span data-ttu-id="35acc-101">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="35acc-101">Suspend-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="35acc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35acc-102">SYNOPSIS</span></span>
<span data-ttu-id="35acc-103">Suspende uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="35acc-103">Suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="35acc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35acc-104">SYNTAX</span></span>

```
Suspend-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35acc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35acc-105">DESCRIPTION</span></span>
<span data-ttu-id="35acc-106">O cmdlet Suspend-AzAnalysisServicesServer suspende uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="35acc-106">The Suspend-AzAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="35acc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35acc-107">EXAMPLES</span></span>

### <span data-ttu-id="35acc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="35acc-108">Example 1</span></span>
```
PS C:\> Suspend-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="35acc-109">Esse comando suspenderá um servidor ativo chamado TestServer no modo de teste do modo de Resource</span><span class="sxs-lookup"><span data-stu-id="35acc-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="35acc-110">OS</span><span class="sxs-lookup"><span data-stu-id="35acc-110">PARAMETERS</span></span>

### <span data-ttu-id="35acc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35acc-111">-DefaultProfile</span></span>
<span data-ttu-id="35acc-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35acc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35acc-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="35acc-113">-Name</span></span>
<span data-ttu-id="35acc-114">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="35acc-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="35acc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35acc-115">-PassThru</span></span>
<span data-ttu-id="35acc-116">Retornará os detalhes do servidor excluído se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="35acc-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="35acc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35acc-117">-ResourceGroupName</span></span>
<span data-ttu-id="35acc-118">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="35acc-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="35acc-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35acc-119">-Confirm</span></span>
<span data-ttu-id="35acc-120">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="35acc-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="35acc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35acc-121">-WhatIf</span></span>
<span data-ttu-id="35acc-122">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="35acc-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="35acc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35acc-123">CommonParameters</span></span>
<span data-ttu-id="35acc-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35acc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35acc-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35acc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35acc-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35acc-126">INPUTS</span></span>

### <span data-ttu-id="35acc-127">System. String</span><span class="sxs-lookup"><span data-stu-id="35acc-127">System.String</span></span>

## <span data-ttu-id="35acc-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35acc-128">OUTPUTS</span></span>

### <span data-ttu-id="35acc-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="35acc-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="35acc-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35acc-130">NOTES</span></span>
<span data-ttu-id="35acc-131">Alias: Suspend-AzAs</span><span class="sxs-lookup"><span data-stu-id="35acc-131">Alias: Suspend-AzAs</span></span>

## <span data-ttu-id="35acc-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35acc-132">RELATED LINKS</span></span>

[<span data-ttu-id="35acc-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="35acc-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="35acc-134">Currículo-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="35acc-134">Resume-AzAnalysisServicesServer</span></span>](./Resume-AzAnalysisServicesServer.md)

