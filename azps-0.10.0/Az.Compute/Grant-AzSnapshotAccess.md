---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: e4283b23fb4a82c17f35354d854c30c3ec1b2329
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776983"
---
# <span data-ttu-id="cbd3f-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="cbd3f-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="cbd3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbd3f-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd3f-103">Concede um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="cbd3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbd3f-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbd3f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cbd3f-105">DESCRIPTION</span></span>
<span data-ttu-id="cbd3f-106">O cmdlet **Grant-AzSnapshotAccess** concede um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="cbd3f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbd3f-107">EXAMPLES</span></span>

### <span data-ttu-id="cbd3f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cbd3f-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="cbd3f-109">Conceda acesso "leitura" ao instantâneo chamado "Snapshot01" no grupo de recursos chamado "ResourceGroup01" para 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="cbd3f-110">OS</span><span class="sxs-lookup"><span data-stu-id="cbd3f-110">PARAMETERS</span></span>

### <span data-ttu-id="cbd3f-111">-Acesso</span><span class="sxs-lookup"><span data-stu-id="cbd3f-111">-Access</span></span>
<span data-ttu-id="cbd3f-112">Especifica o nível de acesso.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd3f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbd3f-113">-AsJob</span></span>
<span data-ttu-id="cbd3f-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cbd3f-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd3f-115">-DefaultProfile</span></span>
<span data-ttu-id="cbd3f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbd3f-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="cbd3f-117">-DurationInSecond</span></span>
<span data-ttu-id="cbd3f-118">Especifica a duração do acesso em segundos.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-118">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd3f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd3f-119">-ResourceGroupName</span></span>
<span data-ttu-id="cbd3f-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd3f-121">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="cbd3f-121">-SnapshotName</span></span>
<span data-ttu-id="cbd3f-122">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd3f-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cbd3f-123">-Confirm</span></span>
<span data-ttu-id="cbd3f-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd3f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbd3f-125">-WhatIf</span></span>
<span data-ttu-id="cbd3f-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbd3f-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd3f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd3f-128">CommonParameters</span></span>
<span data-ttu-id="cbd3f-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbd3f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd3f-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbd3f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd3f-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cbd3f-131">INPUTS</span></span>

### <span data-ttu-id="cbd3f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cbd3f-132">System.String</span></span>

## <span data-ttu-id="cbd3f-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cbd3f-133">OUTPUTS</span></span>

### <span data-ttu-id="cbd3f-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="cbd3f-134">System.Object</span></span>

## <span data-ttu-id="cbd3f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cbd3f-135">NOTES</span></span>

## <span data-ttu-id="cbd3f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbd3f-136">RELATED LINKS</span></span>

