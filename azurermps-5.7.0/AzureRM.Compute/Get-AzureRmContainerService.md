---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: d2a53d221adf7483899056791aefd00b03aca26e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431070"
---
# <span data-ttu-id="23bbb-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="23bbb-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="23bbb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="23bbb-103">Obtém um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="23bbb-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23bbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23bbb-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="23bbb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23bbb-105">DESCRIPTION</span></span>
<span data-ttu-id="23bbb-106">O cmdlet **Get-AzureRmContainerService** recebe um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="23bbb-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="23bbb-107">Você pode exibir as propriedades de um serviço de contêiner, que incluem estado, número de mestres e agentes e nome de domínio totalmente qualificado do mestre e do agente.</span><span class="sxs-lookup"><span data-stu-id="23bbb-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="23bbb-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23bbb-108">EXAMPLES</span></span>

### <span data-ttu-id="23bbb-109">Exemplo 1: obter um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="23bbb-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="23bbb-110">Esse comando obtém um serviço de contêiner chamado CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="23bbb-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="23bbb-111">OS</span><span class="sxs-lookup"><span data-stu-id="23bbb-111">PARAMETERS</span></span>

### <span data-ttu-id="23bbb-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="23bbb-112">-Name</span></span>
<span data-ttu-id="23bbb-113">Especifica o nome do serviço de contêiner que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="23bbb-113">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23bbb-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23bbb-114">-ResourceGroupName</span></span>
<span data-ttu-id="23bbb-115">Especifica o grupo de recursos do serviço de contêiner que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="23bbb-115">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="23bbb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23bbb-116">CommonParameters</span></span>
<span data-ttu-id="23bbb-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23bbb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23bbb-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23bbb-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23bbb-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23bbb-119">INPUTS</span></span>

### <span data-ttu-id="23bbb-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="23bbb-120">None</span></span>
<span data-ttu-id="23bbb-121">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="23bbb-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="23bbb-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23bbb-122">OUTPUTS</span></span>

## <span data-ttu-id="23bbb-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23bbb-123">NOTES</span></span>

## <span data-ttu-id="23bbb-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23bbb-124">RELATED LINKS</span></span>

[<span data-ttu-id="23bbb-125">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="23bbb-125">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="23bbb-126">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="23bbb-126">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="23bbb-127">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="23bbb-127">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


