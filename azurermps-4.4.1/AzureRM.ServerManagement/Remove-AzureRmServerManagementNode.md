---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: B66C7A03-862A-497D-977B-1C43089DE24B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
ms.openlocfilehash: 93efff5a9f317b7d44d071a4dd212d235df02223
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430633"
---
# <span data-ttu-id="e3b8a-101">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="e3b8a-101">Remove-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="e3b8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3b8a-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b8a-103">Remove um nó de gerenciamento de servidor.</span><span class="sxs-lookup"><span data-stu-id="e3b8a-103">Removes a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3b8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3b8a-104">SYNTAX</span></span>

### <span data-ttu-id="e3b8a-105">ByName</span><span class="sxs-lookup"><span data-stu-id="e3b8a-105">ByName</span></span>
```
Remove-AzureRmServerManagementNode [-ResourceGroupName] <String> [-NodeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3b8a-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="e3b8a-106">ByObject</span></span>
```
Remove-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3b8a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3b8a-107">DESCRIPTION</span></span>
<span data-ttu-id="e3b8a-108">O cmdlet **Remove-AzureRmServerManagementNode** remove um nó de gerenciamento do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b8a-108">The **Remove-AzureRmServerManagementNode** cmdlet removes an Azure Server Management node.</span></span>

## <span data-ttu-id="e3b8a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3b8a-109">EXAMPLES</span></span>

## <span data-ttu-id="e3b8a-110">OS</span><span class="sxs-lookup"><span data-stu-id="e3b8a-110">PARAMETERS</span></span>

### <span data-ttu-id="e3b8a-111">-Nó</span><span class="sxs-lookup"><span data-stu-id="e3b8a-111">-Node</span></span>
<span data-ttu-id="e3b8a-112">Especifica o nó para o qual esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e3b8a-112">Specifies the node for which this cmdlet removes.</span></span>

<span data-ttu-id="e3b8a-113">Esse parâmetro pode ser usado em vez dos parâmetros *ResourceGroupName* e *NodeName* .</span><span class="sxs-lookup"><span data-stu-id="e3b8a-113">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b8a-114">-NodeName</span><span class="sxs-lookup"><span data-stu-id="e3b8a-114">-NodeName</span></span>
<span data-ttu-id="e3b8a-115">Especifica o nome do nó para o qual esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e3b8a-115">Specifies the name of the node for which this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b8a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b8a-116">-ResourceGroupName</span></span>
<span data-ttu-id="e3b8a-117">Especifica o nome do grupo de recursos ao qual o nó pertence.</span><span class="sxs-lookup"><span data-stu-id="e3b8a-117">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b8a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b8a-118">-DefaultProfile</span></span>
<span data-ttu-id="e3b8a-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b8a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3b8a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b8a-120">CommonParameters</span></span>
<span data-ttu-id="e3b8a-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3b8a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b8a-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3b8a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b8a-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3b8a-123">INPUTS</span></span>

### <span data-ttu-id="e3b8a-124">Nó</span><span class="sxs-lookup"><span data-stu-id="e3b8a-124">Node</span></span>
<span data-ttu-id="e3b8a-125">O parâmetro ' node ' aceita o valor do tipo ' node ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="e3b8a-125">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="e3b8a-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3b8a-126">OUTPUTS</span></span>

## <span data-ttu-id="e3b8a-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3b8a-127">NOTES</span></span>

## <span data-ttu-id="e3b8a-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3b8a-128">RELATED LINKS</span></span>

[<span data-ttu-id="e3b8a-129">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="e3b8a-129">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="e3b8a-130">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="e3b8a-130">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)


