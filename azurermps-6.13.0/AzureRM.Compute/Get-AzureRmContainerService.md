---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: 0f87254f72d0b5ac22a5770ad3f1a9d03b70fd34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428572"
---
# <span data-ttu-id="6776d-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6776d-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="6776d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6776d-102">SYNOPSIS</span></span>
<span data-ttu-id="6776d-103">Obtém um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="6776d-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6776d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6776d-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6776d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6776d-105">DESCRIPTION</span></span>
<span data-ttu-id="6776d-106">O cmdlet **Get-AzureRmContainerService** recebe um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="6776d-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="6776d-107">Você pode exibir as propriedades de um serviço de contêiner, que incluem estado, número de mestres e agentes e nome de domínio totalmente qualificado do mestre e do agente.</span><span class="sxs-lookup"><span data-stu-id="6776d-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="6776d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6776d-108">EXAMPLES</span></span>

### <span data-ttu-id="6776d-109">Exemplo 1: obter um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="6776d-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="6776d-110">Esse comando obtém um serviço de contêiner chamado CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="6776d-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="6776d-111">OS</span><span class="sxs-lookup"><span data-stu-id="6776d-111">PARAMETERS</span></span>

### <span data-ttu-id="6776d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6776d-112">-DefaultProfile</span></span>
<span data-ttu-id="6776d-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6776d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6776d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="6776d-114">-Name</span></span>
<span data-ttu-id="6776d-115">Especifica o nome do serviço de contêiner que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6776d-115">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6776d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6776d-116">-ResourceGroupName</span></span>
<span data-ttu-id="6776d-117">Especifica o grupo de recursos do serviço de contêiner que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6776d-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6776d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6776d-118">CommonParameters</span></span>
<span data-ttu-id="6776d-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6776d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6776d-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6776d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6776d-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6776d-121">INPUTS</span></span>

### <span data-ttu-id="6776d-122">System. String</span><span class="sxs-lookup"><span data-stu-id="6776d-122">System.String</span></span>

## <span data-ttu-id="6776d-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6776d-123">OUTPUTS</span></span>

### <span data-ttu-id="6776d-124">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="6776d-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="6776d-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6776d-125">NOTES</span></span>

## <span data-ttu-id="6776d-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6776d-126">RELATED LINKS</span></span>

[<span data-ttu-id="6776d-127">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6776d-127">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="6776d-128">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6776d-128">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="6776d-129">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6776d-129">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


