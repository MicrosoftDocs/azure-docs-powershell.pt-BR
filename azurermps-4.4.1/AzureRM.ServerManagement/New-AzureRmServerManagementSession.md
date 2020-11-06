---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 0ae3e221ee39a00381f009f45a9a2f508a552b6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429118"
---
# <span data-ttu-id="b0804-101">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="b0804-101">New-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="b0804-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0804-102">SYNOPSIS</span></span>
<span data-ttu-id="b0804-103">Cria uma sessão de gerenciamento do servidor.</span><span class="sxs-lookup"><span data-stu-id="b0804-103">Creates a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0804-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0804-104">SYNTAX</span></span>

### <span data-ttu-id="b0804-105">ByName</span><span class="sxs-lookup"><span data-stu-id="b0804-105">ByName</span></span>
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0804-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="b0804-106">ByNode</span></span>
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0804-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0804-107">DESCRIPTION</span></span>
<span data-ttu-id="b0804-108">O cmdlet **New-AzureRmServerManagementSession** cria uma sessão de gerenciamento do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0804-108">The **New-AzureRmServerManagementSession** cmdlet creates an Azure Server Management session.</span></span>

## <span data-ttu-id="b0804-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0804-109">EXAMPLES</span></span>

## <span data-ttu-id="b0804-110">OS</span><span class="sxs-lookup"><span data-stu-id="b0804-110">PARAMETERS</span></span>

### <span data-ttu-id="b0804-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="b0804-111">-Credential</span></span>
<span data-ttu-id="b0804-112">Especifica um objeto **PSCredential** para a conexão com a sessão de gerenciamento do servidor.</span><span class="sxs-lookup"><span data-stu-id="b0804-112">Specifies a **PSCredential** object for the connection to the Server Management Session.</span></span>
<span data-ttu-id="b0804-113">Para obter um objeto de credencial, use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="b0804-113">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="b0804-114">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="b0804-114">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0804-115">-Nó</span><span class="sxs-lookup"><span data-stu-id="b0804-115">-Node</span></span>
<span data-ttu-id="b0804-116">Especifica o nó para o qual esse cmdlet cria a sessão.</span><span class="sxs-lookup"><span data-stu-id="b0804-116">Specifies the node for which this cmdlet creates the session on.</span></span>

<span data-ttu-id="b0804-117">Esse parâmetro pode ser usado em vez dos parâmetros *ResourceGroupName* e *NodeName* .</span><span class="sxs-lookup"><span data-stu-id="b0804-117">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

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

### <span data-ttu-id="b0804-118">-NodeName</span><span class="sxs-lookup"><span data-stu-id="b0804-118">-NodeName</span></span>
<span data-ttu-id="b0804-119">Especifica o nome do nó para o qual esse cmdlet cria uma sessão.</span><span class="sxs-lookup"><span data-stu-id="b0804-119">Specifies the name of the node for which this cmdlet creates a session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0804-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0804-120">-ResourceGroupName</span></span>
<span data-ttu-id="b0804-121">Especifica o grupo de recursos do nó para o qual esse cmdlet cria uma sessão.</span><span class="sxs-lookup"><span data-stu-id="b0804-121">Specifies the resource group of the node that this cmdlet creates a session for.</span></span>

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

### <span data-ttu-id="b0804-122">-SESSIONNAME</span><span class="sxs-lookup"><span data-stu-id="b0804-122">-SessionName</span></span>
<span data-ttu-id="b0804-123">Especifica o nome a ser usado para a sessão.</span><span class="sxs-lookup"><span data-stu-id="b0804-123">Specifies the name to use for the session.</span></span>

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

### <span data-ttu-id="b0804-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0804-124">-DefaultProfile</span></span>
<span data-ttu-id="b0804-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0804-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0804-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0804-126">CommonParameters</span></span>
<span data-ttu-id="b0804-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0804-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0804-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0804-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0804-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0804-129">INPUTS</span></span>

### <span data-ttu-id="b0804-130">Nó</span><span class="sxs-lookup"><span data-stu-id="b0804-130">Node</span></span>
<span data-ttu-id="b0804-131">O parâmetro ' node ' aceita o valor do tipo ' node ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="b0804-131">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="b0804-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0804-132">OUTPUTS</span></span>

### <span data-ttu-id="b0804-133">Microsoft. Azure. Commands. ServerManagement. Model. Session</span><span class="sxs-lookup"><span data-stu-id="b0804-133">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="b0804-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0804-134">NOTES</span></span>

## <span data-ttu-id="b0804-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0804-135">RELATED LINKS</span></span>

