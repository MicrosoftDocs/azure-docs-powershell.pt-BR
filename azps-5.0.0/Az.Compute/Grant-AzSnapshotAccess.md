---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: a431428c670dba7e0bfb152bde0cae22f47d8099
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116807"
---
# <span data-ttu-id="5b2bd-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="5b2bd-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="5b2bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b2bd-102">SYNOPSIS</span></span>
<span data-ttu-id="5b2bd-103">Concede um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="5b2bd-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="5b2bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b2bd-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b2bd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5b2bd-105">DESCRIPTION</span></span>
<span data-ttu-id="5b2bd-106">O cmdlet **Grant-AzSnapshotAccess** concede um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="5b2bd-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="5b2bd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b2bd-107">EXAMPLES</span></span>

### <span data-ttu-id="5b2bd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5b2bd-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="5b2bd-109">Conceda acesso "leitura" ao instantâneo chamado "Snapshot01" no grupo de recursos chamado "ResourceGroup01" para 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="5b2bd-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="5b2bd-110">OS</span><span class="sxs-lookup"><span data-stu-id="5b2bd-110">PARAMETERS</span></span>

### <span data-ttu-id="5b2bd-111">-Acesso</span><span class="sxs-lookup"><span data-stu-id="5b2bd-111">-Access</span></span>
<span data-ttu-id="5b2bd-112">Especifica o nível de acesso.</span><span class="sxs-lookup"><span data-stu-id="5b2bd-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b2bd-113">-AsJob</span></span>
<span data-ttu-id="5b2bd-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5b2bd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b2bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b2bd-115">-DefaultProfile</span></span>
<span data-ttu-id="5b2bd-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b2bd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bd-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="5b2bd-117">-DurationInSecond</span></span>
<span data-ttu-id="5b2bd-118">Especifica a duração do acesso em segundos.</span><span class="sxs-lookup"><span data-stu-id="5b2bd-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b2bd-119">-ResourceGroupName</span></span>
<span data-ttu-id="5b2bd-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5b2bd-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bd-121">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="5b2bd-121">-SnapshotName</span></span>
<span data-ttu-id="5b2bd-122">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="5b2bd-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bd-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5b2bd-123">-Confirm</span></span>
<span data-ttu-id="5b2bd-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b2bd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b2bd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b2bd-125">-WhatIf</span></span>
<span data-ttu-id="5b2bd-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5b2bd-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b2bd-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5b2bd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b2bd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b2bd-128">CommonParameters</span></span>
<span data-ttu-id="5b2bd-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b2bd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b2bd-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b2bd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b2bd-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5b2bd-131">INPUTS</span></span>

### <span data-ttu-id="5b2bd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5b2bd-132">System.String</span></span>

## <span data-ttu-id="5b2bd-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5b2bd-133">OUTPUTS</span></span>

### <span data-ttu-id="5b2bd-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="5b2bd-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="5b2bd-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5b2bd-135">NOTES</span></span>

## <span data-ttu-id="5b2bd-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b2bd-136">RELATED LINKS</span></span>
