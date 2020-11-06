---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8942D757-B204-49CE-BCDE-68C3722913B3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
ms.openlocfilehash: e32f9268309562b45e13df164631e18d28cceb0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428781"
---
# <span data-ttu-id="a2a24-101">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="a2a24-101">Get-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="a2a24-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2a24-102">SYNOPSIS</span></span>
<span data-ttu-id="a2a24-103">Obtém uma sessão de gerenciamento do servidor.</span><span class="sxs-lookup"><span data-stu-id="a2a24-103">Gets a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2a24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2a24-104">SYNTAX</span></span>

### <span data-ttu-id="a2a24-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="a2a24-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2a24-106">BySession</span><span class="sxs-lookup"><span data-stu-id="a2a24-106">BySession</span></span>
```
Get-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2a24-107">ByNode</span><span class="sxs-lookup"><span data-stu-id="a2a24-107">ByNode</span></span>
```
Get-AzureRmServerManagementSession [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2a24-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2a24-108">DESCRIPTION</span></span>
<span data-ttu-id="a2a24-109">O cmdlet **Get-AzureRmServerManagementSession** Obtém uma única sessão de gerenciamento do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a24-109">The **Get-AzureRmServerManagementSession** cmdlet gets a single Azure Server Management session.</span></span>

## <span data-ttu-id="a2a24-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2a24-110">EXAMPLES</span></span>

## <span data-ttu-id="a2a24-111">OS</span><span class="sxs-lookup"><span data-stu-id="a2a24-111">PARAMETERS</span></span>

### <span data-ttu-id="a2a24-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2a24-112">-DefaultProfile</span></span>
<span data-ttu-id="a2a24-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a24-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2a24-114">-Nó</span><span class="sxs-lookup"><span data-stu-id="a2a24-114">-Node</span></span>
<span data-ttu-id="a2a24-115">Especifica um objeto de **nó** existente que é usado para obter os parâmetros *ResourceGroupName* e *node NodeName* .</span><span class="sxs-lookup"><span data-stu-id="a2a24-115">Specifies an existing **Node** object that is used to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>
<span data-ttu-id="a2a24-116">Você também deve especificar um valor para o parâmetro *SessionName* .</span><span class="sxs-lookup"><span data-stu-id="a2a24-116">You must also specify a value for the *SessionName* parameter.</span></span>

```yaml
Type: Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a24-117">-NodeName</span><span class="sxs-lookup"><span data-stu-id="a2a24-117">-NodeName</span></span>
<span data-ttu-id="a2a24-118">Especifica o nome do nó no qual a sessão está localizada.</span><span class="sxs-lookup"><span data-stu-id="a2a24-118">Specifies the name of the node where the session is located.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a24-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2a24-119">-ResourceGroupName</span></span>
<span data-ttu-id="a2a24-120">Especifica o nome do grupo de recursos para o qual esse cmdlet obtém a sessão de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a2a24-120">Specifies the name of the resource group for which this cmdlet gets the retrieve the session.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a24-121">-Sessão</span><span class="sxs-lookup"><span data-stu-id="a2a24-121">-Session</span></span>
<span data-ttu-id="a2a24-122">Especifica um objeto **Session** existente que é usado para obter o *ResourceGroupName* , *NodeName* e os parâmetros *SessionName* .</span><span class="sxs-lookup"><span data-stu-id="a2a24-122">Specifies an existing **Session** object that is used to get the *ResourceGroupName* , the *NodeName* , and the *SessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a24-123">-SESSIONNAME</span><span class="sxs-lookup"><span data-stu-id="a2a24-123">-SessionName</span></span>
<span data-ttu-id="a2a24-124">Especifica o nome da sessão na qual esse cmdlet se obtém.</span><span class="sxs-lookup"><span data-stu-id="a2a24-124">Specifies the name of the session in which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySession
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2a24-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2a24-125">CommonParameters</span></span>
<span data-ttu-id="a2a24-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2a24-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2a24-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2a24-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2a24-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2a24-128">INPUTS</span></span>

### <span data-ttu-id="a2a24-129">Nó</span><span class="sxs-lookup"><span data-stu-id="a2a24-129">Node</span></span>
<span data-ttu-id="a2a24-130">O parâmetro ' node ' aceita o valor do tipo ' node ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="a2a24-130">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

### <span data-ttu-id="a2a24-131">Sessão</span><span class="sxs-lookup"><span data-stu-id="a2a24-131">Session</span></span>
<span data-ttu-id="a2a24-132">O parâmetro ' Session ' aceita o valor do tipo ' Session ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="a2a24-132">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="a2a24-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2a24-133">OUTPUTS</span></span>

### <span data-ttu-id="a2a24-134">Microsoft. Azure. Commands. ServerManagement. Model. Session</span><span class="sxs-lookup"><span data-stu-id="a2a24-134">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="a2a24-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2a24-135">NOTES</span></span>

## <span data-ttu-id="a2a24-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2a24-136">RELATED LINKS</span></span>

[<span data-ttu-id="a2a24-137">Cmdlets de gerenciamento do Azure Server</span><span class="sxs-lookup"><span data-stu-id="a2a24-137">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)

