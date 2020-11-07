---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 1a0daa4bf336ba970c12c24db3d5aab73641aaea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777055"
---
# <span data-ttu-id="0fcc8-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0fcc8-101">Get-AzContainerService</span></span>

## <span data-ttu-id="0fcc8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0fcc8-102">SYNOPSIS</span></span>
<span data-ttu-id="0fcc8-103">Obtém um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="0fcc8-103">Gets a container service.</span></span>

## <span data-ttu-id="0fcc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0fcc8-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fcc8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0fcc8-105">DESCRIPTION</span></span>
<span data-ttu-id="0fcc8-106">O cmdlet **Get-AzContainerService** recebe um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="0fcc8-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="0fcc8-107">Você pode exibir as propriedades de um serviço de contêiner, que incluem estado, número de mestres e agentes e nome de domínio totalmente qualificado do mestre e do agente.</span><span class="sxs-lookup"><span data-stu-id="0fcc8-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="0fcc8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0fcc8-108">EXAMPLES</span></span>

### <span data-ttu-id="0fcc8-109">Exemplo 1: obter um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="0fcc8-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="0fcc8-110">Esse comando obtém um serviço de contêiner chamado CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="0fcc8-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="0fcc8-111">OS</span><span class="sxs-lookup"><span data-stu-id="0fcc8-111">PARAMETERS</span></span>

### <span data-ttu-id="0fcc8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fcc8-112">-DefaultProfile</span></span>
<span data-ttu-id="0fcc8-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0fcc8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fcc8-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="0fcc8-114">-Name</span></span>
<span data-ttu-id="0fcc8-115">Especifica o nome do serviço de contêiner que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="0fcc8-115">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0fcc8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fcc8-116">-ResourceGroupName</span></span>
<span data-ttu-id="0fcc8-117">Especifica o grupo de recursos do serviço de contêiner que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="0fcc8-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0fcc8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fcc8-118">CommonParameters</span></span>
<span data-ttu-id="0fcc8-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fcc8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fcc8-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fcc8-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fcc8-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0fcc8-121">INPUTS</span></span>

### <span data-ttu-id="0fcc8-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0fcc8-122">None</span></span>
<span data-ttu-id="0fcc8-123">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="0fcc8-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0fcc8-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0fcc8-124">OUTPUTS</span></span>

### <span data-ttu-id="0fcc8-125">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="0fcc8-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="0fcc8-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0fcc8-126">NOTES</span></span>

## <span data-ttu-id="0fcc8-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0fcc8-127">RELATED LINKS</span></span>

[<span data-ttu-id="0fcc8-128">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0fcc8-128">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="0fcc8-129">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0fcc8-129">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="0fcc8-130">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0fcc8-130">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


