---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: b60abc403beea938e24ffaa59e634a36611d150b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430369"
---
# <span data-ttu-id="0f2e2-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="0f2e2-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="0f2e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f2e2-102">SYNOPSIS</span></span>
<span data-ttu-id="0f2e2-103">Concede um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="0f2e2-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f2e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f2e2-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f2e2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f2e2-105">DESCRIPTION</span></span>
<span data-ttu-id="0f2e2-106">O cmdlet **Grant-AzureRmSnapshotAccess** concede um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="0f2e2-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="0f2e2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f2e2-107">EXAMPLES</span></span>

### <span data-ttu-id="0f2e2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f2e2-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="0f2e2-109">Conceda acesso "leitura" ao instantâneo chamado "Snapshot01" no grupo de recursos chamado "ResourceGroup01" para 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="0f2e2-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="0f2e2-110">OS</span><span class="sxs-lookup"><span data-stu-id="0f2e2-110">PARAMETERS</span></span>

### <span data-ttu-id="0f2e2-111">-Acesso</span><span class="sxs-lookup"><span data-stu-id="0f2e2-111">-Access</span></span>
<span data-ttu-id="0f2e2-112">Especifica o nível de acesso.</span><span class="sxs-lookup"><span data-stu-id="0f2e2-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2e2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f2e2-113">-AsJob</span></span>
<span data-ttu-id="0f2e2-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0f2e2-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f2e2-115">-DefaultProfile</span></span>
<span data-ttu-id="0f2e2-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f2e2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f2e2-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="0f2e2-117">-DurationInSecond</span></span>
<span data-ttu-id="0f2e2-118">Especifica a duração do acesso em segundos.</span><span class="sxs-lookup"><span data-stu-id="0f2e2-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f2e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="0f2e2-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0f2e2-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2e2-121">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="0f2e2-121">-SnapshotName</span></span>
<span data-ttu-id="0f2e2-122">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="0f2e2-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2e2-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0f2e2-123">-Confirm</span></span>
<span data-ttu-id="0f2e2-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f2e2-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2e2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f2e2-125">-WhatIf</span></span>
<span data-ttu-id="0f2e2-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0f2e2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f2e2-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f2e2-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2e2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f2e2-128">CommonParameters</span></span>
<span data-ttu-id="0f2e2-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f2e2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f2e2-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f2e2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f2e2-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f2e2-131">INPUTS</span></span>

### <span data-ttu-id="0f2e2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0f2e2-132">System.String</span></span>

## <span data-ttu-id="0f2e2-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f2e2-133">OUTPUTS</span></span>

### <span data-ttu-id="0f2e2-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="0f2e2-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="0f2e2-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f2e2-135">NOTES</span></span>

## <span data-ttu-id="0f2e2-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f2e2-136">RELATED LINKS</span></span>
