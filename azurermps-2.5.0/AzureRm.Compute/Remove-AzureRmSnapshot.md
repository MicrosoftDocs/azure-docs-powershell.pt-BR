---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: cf63923b278f009cb676c79642882e64e6b8e303
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786138"
---
# <span data-ttu-id="dc387-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="dc387-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="dc387-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc387-102">SYNOPSIS</span></span>
<span data-ttu-id="dc387-103">Remove um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="dc387-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc387-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc387-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc387-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc387-105">DESCRIPTION</span></span>
<span data-ttu-id="dc387-106">O cmdlet **Remove-AzureRmSnapshot** remove um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="dc387-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="dc387-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc387-107">EXAMPLES</span></span>

### <span data-ttu-id="dc387-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dc387-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="dc387-109">Este comando Remove o instantâneo chamado "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="dc387-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="dc387-110">OS</span><span class="sxs-lookup"><span data-stu-id="dc387-110">PARAMETERS</span></span>

### <span data-ttu-id="dc387-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc387-111">-AsJob</span></span>
<span data-ttu-id="dc387-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="dc387-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="dc387-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc387-113">-DefaultProfile</span></span>
<span data-ttu-id="dc387-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc387-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc387-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dc387-115">-Force</span></span>
<span data-ttu-id="dc387-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc387-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dc387-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc387-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc387-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc387-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dc387-119">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="dc387-119">-SnapshotName</span></span>
<span data-ttu-id="dc387-120">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="dc387-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="dc387-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dc387-121">-Confirm</span></span>
<span data-ttu-id="dc387-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc387-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc387-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc387-123">-WhatIf</span></span>
<span data-ttu-id="dc387-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dc387-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc387-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dc387-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc387-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc387-126">CommonParameters</span></span>
<span data-ttu-id="dc387-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc387-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc387-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc387-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc387-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc387-129">INPUTS</span></span>

### <span data-ttu-id="dc387-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dc387-130">System.String</span></span>

## <span data-ttu-id="dc387-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc387-131">OUTPUTS</span></span>

### <span data-ttu-id="dc387-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="dc387-132">System.Object</span></span>

## <span data-ttu-id="dc387-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc387-133">NOTES</span></span>

## <span data-ttu-id="dc387-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc387-134">RELATED LINKS</span></span>

