---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 35b8788c67098a45f6a5373e90b7a93fbcbc4703
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427050"
---
# <span data-ttu-id="c4226-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c4226-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="c4226-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4226-102">SYNOPSIS</span></span>
<span data-ttu-id="c4226-103">Suspende uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="c4226-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4226-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4226-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4226-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4226-105">DESCRIPTION</span></span>
<span data-ttu-id="c4226-106">O cmdlet Suspend-AzureRmAnalysisServicesServer suspende uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="c4226-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="c4226-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4226-107">EXAMPLES</span></span>

### <span data-ttu-id="c4226-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c4226-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="c4226-109">Esse comando suspenderá um servidor ativo chamado TestServer no modo de teste do modo de Resource</span><span class="sxs-lookup"><span data-stu-id="c4226-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="c4226-110">OS</span><span class="sxs-lookup"><span data-stu-id="c4226-110">PARAMETERS</span></span>

### <span data-ttu-id="c4226-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4226-111">-Name</span></span>
<span data-ttu-id="c4226-112">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="c4226-112">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4226-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4226-113">-PassThru</span></span>
<span data-ttu-id="c4226-114">Retornará os detalhes do servidor excluído se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="c4226-114">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4226-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4226-115">-ResourceGroupName</span></span>
<span data-ttu-id="c4226-116">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="c4226-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4226-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c4226-117">-Confirm</span></span>
<span data-ttu-id="c4226-118">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="c4226-118">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4226-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4226-119">-WhatIf</span></span>
<span data-ttu-id="c4226-120">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="c4226-120">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4226-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4226-121">CommonParameters</span></span>
<span data-ttu-id="c4226-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4226-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4226-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4226-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4226-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4226-124">INPUTS</span></span>

## <span data-ttu-id="c4226-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4226-125">OUTPUTS</span></span>

### <span data-ttu-id="c4226-126">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c4226-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="c4226-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4226-127">NOTES</span></span>
<span data-ttu-id="c4226-128">Alias: Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="c4226-128">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="c4226-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4226-129">RELATED LINKS</span></span>

[<span data-ttu-id="c4226-130">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c4226-130">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="c4226-131">Currículo-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c4226-131">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)

