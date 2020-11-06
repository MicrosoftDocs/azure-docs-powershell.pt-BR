---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 99f8eaae633f984cdd522576a3f65bf894143bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427055"
---
# <span data-ttu-id="f564d-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f564d-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="f564d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f564d-102">SYNOPSIS</span></span>
<span data-ttu-id="f564d-103">Retoma uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f564d-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f564d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f564d-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f564d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f564d-105">DESCRIPTION</span></span>
<span data-ttu-id="f564d-106">O cmdlet Resume-AzureRmAnalysisServicesServer retoma uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f564d-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="f564d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f564d-107">EXAMPLES</span></span>

### <span data-ttu-id="f564d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f564d-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="f564d-109">Esse comando retomará um servidor pausado chamado TestServer no de teste do meu nome do o-botão</span><span class="sxs-lookup"><span data-stu-id="f564d-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="f564d-110">OS</span><span class="sxs-lookup"><span data-stu-id="f564d-110">PARAMETERS</span></span>

### <span data-ttu-id="f564d-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="f564d-111">-Name</span></span>
<span data-ttu-id="f564d-112">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f564d-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="f564d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f564d-113">-PassThru</span></span>
<span data-ttu-id="f564d-114">Retornará os detalhes do servidor excluído se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="f564d-114">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="f564d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f564d-115">-ResourceGroupName</span></span>
<span data-ttu-id="f564d-116">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="f564d-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="f564d-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f564d-117">-Confirm</span></span>
<span data-ttu-id="f564d-118">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="f564d-118">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="f564d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f564d-119">-WhatIf</span></span>
<span data-ttu-id="f564d-120">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="f564d-120">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="f564d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f564d-121">CommonParameters</span></span>
<span data-ttu-id="f564d-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f564d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f564d-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f564d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f564d-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f564d-124">INPUTS</span></span>

## <span data-ttu-id="f564d-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f564d-125">OUTPUTS</span></span>

### <span data-ttu-id="f564d-126">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f564d-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="f564d-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f564d-127">NOTES</span></span>
<span data-ttu-id="f564d-128">Alias: Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="f564d-128">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="f564d-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f564d-129">RELATED LINKS</span></span>

[<span data-ttu-id="f564d-130">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f564d-130">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="f564d-131">Suspender-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f564d-131">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
