---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: a75eafd57ff7351aa1858114da1cdc7f44b9875c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440950"
---
# <span data-ttu-id="a2922-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a2922-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="a2922-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2922-102">SYNOPSIS</span></span>
<span data-ttu-id="a2922-103">Obtém coletas de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="a2922-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2922-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2922-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2922-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2922-105">DESCRIPTION</span></span>
<span data-ttu-id="a2922-106">O cmdlet **Get-AzureRmSchedulerJobCollection** Obtém as coleções de trabalhos no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="a2922-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="a2922-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2922-107">EXAMPLES</span></span>

## <span data-ttu-id="a2922-108">OS</span><span class="sxs-lookup"><span data-stu-id="a2922-108">PARAMETERS</span></span>

### <span data-ttu-id="a2922-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="a2922-109">-JobCollectionName</span></span>
<span data-ttu-id="a2922-110">Especifica o nome de uma coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="a2922-110">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2922-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2922-111">-ResourceGroupName</span></span>
<span data-ttu-id="a2922-112">Especifica o grupo de recursos a partir do qual esse cmdlet obtém as coletas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a2922-112">Specifies resource group from which this cmdlet gets job collections.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2922-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2922-113">-DefaultProfile</span></span>
<span data-ttu-id="a2922-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2922-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2922-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2922-115">CommonParameters</span></span>
<span data-ttu-id="a2922-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2922-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2922-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2922-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2922-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2922-118">INPUTS</span></span>

## <span data-ttu-id="a2922-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2922-119">OUTPUTS</span></span>

### <span data-ttu-id="a2922-120">System. Object</span><span class="sxs-lookup"><span data-stu-id="a2922-120">System.Object</span></span>

## <span data-ttu-id="a2922-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2922-121">NOTES</span></span>

## <span data-ttu-id="a2922-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2922-122">RELATED LINKS</span></span>

[<span data-ttu-id="a2922-123">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a2922-123">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a2922-124">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a2922-124">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a2922-125">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a2922-125">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a2922-126">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a2922-126">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a2922-127">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a2922-127">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


