---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 4EE30890-B09B-4811-88AD-4BF4FD47E431
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
ms.openlocfilehash: ab49458426b7035a20e63ca62d86124d79291b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430649"
---
# <span data-ttu-id="d5b6b-101">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="d5b6b-101">Get-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="d5b6b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="d5b6b-103">Obtém um ou mais nós de gerenciamento do servidor.</span><span class="sxs-lookup"><span data-stu-id="d5b6b-103">Gets one or more Server Management nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5b6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5b6b-104">SYNTAX</span></span>

### <span data-ttu-id="d5b6b-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="d5b6b-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementNode [[-ResourceGroupName] <String>] [[-NodeName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5b6b-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="d5b6b-106">ByNode</span></span>
```
Get-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5b6b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5b6b-107">DESCRIPTION</span></span>
<span data-ttu-id="d5b6b-108">O cmdlet **Get-AzureRmServerManagementNode** Obtém um ou mais nós de gerenciamento do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="d5b6b-108">The **Get-AzureRmServerManagementNode** cmdlet gets one or more Azure Server Management nodes.</span></span>

## <span data-ttu-id="d5b6b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5b6b-109">EXAMPLES</span></span>

## <span data-ttu-id="d5b6b-110">OS</span><span class="sxs-lookup"><span data-stu-id="d5b6b-110">PARAMETERS</span></span>

### <span data-ttu-id="d5b6b-111">-Nó</span><span class="sxs-lookup"><span data-stu-id="d5b6b-111">-Node</span></span>
<span data-ttu-id="d5b6b-112">Especifica um nó existente do qual obter os parâmetros *ResourceGroupName* e *node Nodes* .</span><span class="sxs-lookup"><span data-stu-id="d5b6b-112">Specifies an existing node from which to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b6b-113">-NodeName</span><span class="sxs-lookup"><span data-stu-id="d5b6b-113">-NodeName</span></span>
<span data-ttu-id="d5b6b-114">Especifica o nome do nó para o qual esse cmdlet se obtém.</span><span class="sxs-lookup"><span data-stu-id="d5b6b-114">Specifies the name of the node for which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b6b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5b6b-115">-ResourceGroupName</span></span>
<span data-ttu-id="d5b6b-116">Especifica o nome do grupo de recursos ao qual os nós pertencem.</span><span class="sxs-lookup"><span data-stu-id="d5b6b-116">Specifies the name of the resource group in which the nodes belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b6b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5b6b-117">-DefaultProfile</span></span>
<span data-ttu-id="d5b6b-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5b6b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5b6b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5b6b-119">CommonParameters</span></span>
<span data-ttu-id="d5b6b-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5b6b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5b6b-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5b6b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5b6b-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5b6b-122">INPUTS</span></span>

### <span data-ttu-id="d5b6b-123">Nó</span><span class="sxs-lookup"><span data-stu-id="d5b6b-123">Node</span></span>
<span data-ttu-id="d5b6b-124">O parâmetro ' node ' aceita o valor do tipo ' node ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="d5b6b-124">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="d5b6b-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5b6b-125">OUTPUTS</span></span>

### <span data-ttu-id="d5b6b-126">Microsoft. Azure. Commands. ServerManagement. Model. Node</span><span class="sxs-lookup"><span data-stu-id="d5b6b-126">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="d5b6b-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5b6b-127">NOTES</span></span>

## <span data-ttu-id="d5b6b-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5b6b-128">RELATED LINKS</span></span>

[<span data-ttu-id="d5b6b-129">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="d5b6b-129">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)

[<span data-ttu-id="d5b6b-130">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="d5b6b-130">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


