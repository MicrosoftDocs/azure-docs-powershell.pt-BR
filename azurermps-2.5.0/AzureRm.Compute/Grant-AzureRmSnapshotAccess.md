---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermsnapshotaccess
schema: 2.0.0
ms.openlocfilehash: b1957543c959a18c9fd0fe4fc12de02064ffdcf0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785988"
---
# <span data-ttu-id="032e4-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="032e4-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="032e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="032e4-102">SYNOPSIS</span></span>
<span data-ttu-id="032e4-103">Concede um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="032e4-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="032e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="032e4-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="032e4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="032e4-105">DESCRIPTION</span></span>
<span data-ttu-id="032e4-106">O cmdlet **Grant-AzureRmSnapshotAccess** concede um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="032e4-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="032e4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="032e4-107">EXAMPLES</span></span>

### <span data-ttu-id="032e4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="032e4-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="032e4-109">Conceda acesso "leitura" ao instantâneo chamado "Snapshot01" no grupo de recursos chamado "ResourceGroup01" para 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="032e4-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="032e4-110">OS</span><span class="sxs-lookup"><span data-stu-id="032e4-110">PARAMETERS</span></span>

### <span data-ttu-id="032e4-111">-Acesso</span><span class="sxs-lookup"><span data-stu-id="032e4-111">-Access</span></span>
<span data-ttu-id="032e4-112">Especifica o nível de acesso.</span><span class="sxs-lookup"><span data-stu-id="032e4-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="032e4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="032e4-113">-AsJob</span></span>
<span data-ttu-id="032e4-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="032e4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="032e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="032e4-115">-DefaultProfile</span></span>
<span data-ttu-id="032e4-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="032e4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="032e4-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="032e4-117">-DurationInSecond</span></span>
<span data-ttu-id="032e4-118">Especifica a duração do acesso em segundos.</span><span class="sxs-lookup"><span data-stu-id="032e4-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="032e4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="032e4-119">-ResourceGroupName</span></span>
<span data-ttu-id="032e4-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="032e4-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="032e4-121">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="032e4-121">-SnapshotName</span></span>
<span data-ttu-id="032e4-122">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="032e4-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="032e4-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="032e4-123">-Confirm</span></span>
<span data-ttu-id="032e4-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="032e4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="032e4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="032e4-125">-WhatIf</span></span>
<span data-ttu-id="032e4-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="032e4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="032e4-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="032e4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="032e4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="032e4-128">CommonParameters</span></span>
<span data-ttu-id="032e4-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="032e4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="032e4-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="032e4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="032e4-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="032e4-131">INPUTS</span></span>

### <span data-ttu-id="032e4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="032e4-132">System.String</span></span>

## <span data-ttu-id="032e4-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="032e4-133">OUTPUTS</span></span>

### <span data-ttu-id="032e4-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="032e4-134">System.Object</span></span>

## <span data-ttu-id="032e4-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="032e4-135">NOTES</span></span>

## <span data-ttu-id="032e4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="032e4-136">RELATED LINKS</span></span>

