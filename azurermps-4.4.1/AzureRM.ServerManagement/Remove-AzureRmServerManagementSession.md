---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 7476E6DC-6DE6-4199-A680-5717053A8CC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
ms.openlocfilehash: d34678b6ff7996eabf807c92a84d647af15f6a71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430632"
---
# <span data-ttu-id="1f1bf-101">Remove-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="1f1bf-101">Remove-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="1f1bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f1bf-102">SYNOPSIS</span></span>
<span data-ttu-id="1f1bf-103">Remove uma sessão de gerenciamento do servidor.</span><span class="sxs-lookup"><span data-stu-id="1f1bf-103">Removes a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f1bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f1bf-104">SYNTAX</span></span>

### <span data-ttu-id="1f1bf-105">ByName</span><span class="sxs-lookup"><span data-stu-id="1f1bf-105">ByName</span></span>
```
Remove-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f1bf-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="1f1bf-106">ByObject</span></span>
```
Remove-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f1bf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f1bf-107">DESCRIPTION</span></span>
<span data-ttu-id="1f1bf-108">O cmdlet **Remove-AzureRmServerManagementSession** remove uma sessão de gerenciamento do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="1f1bf-108">The **Remove-AzureRmServerManagementSession** cmdlet removes an Azure Server Management session.</span></span>

## <span data-ttu-id="1f1bf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f1bf-109">EXAMPLES</span></span>

## <span data-ttu-id="1f1bf-110">OS</span><span class="sxs-lookup"><span data-stu-id="1f1bf-110">PARAMETERS</span></span>

### <span data-ttu-id="1f1bf-111">-NodeName</span><span class="sxs-lookup"><span data-stu-id="1f1bf-111">-NodeName</span></span>
<span data-ttu-id="1f1bf-112">Especifica o nome do nó em que esse cmdlet Remove a sessão.</span><span class="sxs-lookup"><span data-stu-id="1f1bf-112">Specifies the name of the node on which this cmdlet removes the session.</span></span>

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

### <span data-ttu-id="1f1bf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f1bf-113">-ResourceGroupName</span></span>
<span data-ttu-id="1f1bf-114">Especifica o nome do grupo de recursos ao qual a sessão pertence.</span><span class="sxs-lookup"><span data-stu-id="1f1bf-114">Specifies the name of the resource group that the session belongs to.</span></span>

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

### <span data-ttu-id="1f1bf-115">-Sessão</span><span class="sxs-lookup"><span data-stu-id="1f1bf-115">-Session</span></span>
<span data-ttu-id="1f1bf-116">Especifica a sessão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="1f1bf-116">Specifies the session that this cmdlet removes.</span></span>

<span data-ttu-id="1f1bf-117">Esse parâmetro pode ser usado em vez dos parâmetros *ResourceGroupName* , *NodeName* e *SessionName* .</span><span class="sxs-lookup"><span data-stu-id="1f1bf-117">This parameter may be used instead of the *ResourceGroupName* , *NodeName* and *SessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f1bf-118">-SESSIONNAME</span><span class="sxs-lookup"><span data-stu-id="1f1bf-118">-SessionName</span></span>
<span data-ttu-id="1f1bf-119">Especifica o nome da sessão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="1f1bf-119">Specifies the name of the session that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f1bf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f1bf-120">-DefaultProfile</span></span>
<span data-ttu-id="1f1bf-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f1bf-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f1bf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f1bf-122">CommonParameters</span></span>
<span data-ttu-id="1f1bf-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f1bf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f1bf-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f1bf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f1bf-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f1bf-125">INPUTS</span></span>

### <span data-ttu-id="1f1bf-126">Sessão</span><span class="sxs-lookup"><span data-stu-id="1f1bf-126">Session</span></span>
<span data-ttu-id="1f1bf-127">O parâmetro ' Session ' aceita o valor do tipo ' Session ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1f1bf-127">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="1f1bf-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f1bf-128">OUTPUTS</span></span>

## <span data-ttu-id="1f1bf-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f1bf-129">NOTES</span></span>

## <span data-ttu-id="1f1bf-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f1bf-130">RELATED LINKS</span></span>

[<span data-ttu-id="1f1bf-131">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="1f1bf-131">Get-AzureRmServerManagementSession</span></span>](./Get-AzureRmServerManagementSession.md)

[<span data-ttu-id="1f1bf-132">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="1f1bf-132">New-AzureRmServerManagementSession</span></span>](./New-AzureRmServerManagementSession.md)


