---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermdisk
schema: 2.0.0
ms.openlocfilehash: 5987e92e281dd892ebc56c0a18ca59fc99cfc82d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786146"
---
# <span data-ttu-id="4c0e4-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="4c0e4-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="4c0e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c0e4-102">SYNOPSIS</span></span>
<span data-ttu-id="4c0e4-103">Remove um disco.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c0e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c0e4-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c0e4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c0e4-105">DESCRIPTION</span></span>
<span data-ttu-id="4c0e4-106">O cmdlet **Remove-AzureRmDisk** remove um disco.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="4c0e4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c0e4-107">EXAMPLES</span></span>

### <span data-ttu-id="4c0e4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4c0e4-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="4c0e4-109">Este comando Remove o disco chamado "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="4c0e4-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4c0e4-110">OS</span><span class="sxs-lookup"><span data-stu-id="4c0e4-110">PARAMETERS</span></span>

### <span data-ttu-id="4c0e4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c0e4-111">-AsJob</span></span>
<span data-ttu-id="4c0e4-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4c0e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c0e4-113">-DefaultProfile</span></span>
<span data-ttu-id="4c0e4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c0e4-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="4c0e4-115">-DiskName</span></span>
<span data-ttu-id="4c0e4-116">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="4c0e4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4c0e4-117">-Force</span></span>
<span data-ttu-id="4c0e4-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4c0e4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c0e4-119">-ResourceGroupName</span></span>
<span data-ttu-id="4c0e4-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4c0e4-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4c0e4-121">-Confirm</span></span>
<span data-ttu-id="4c0e4-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c0e4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c0e4-123">-WhatIf</span></span>
<span data-ttu-id="4c0e4-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c0e4-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c0e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c0e4-126">CommonParameters</span></span>
<span data-ttu-id="4c0e4-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c0e4-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c0e4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c0e4-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c0e4-129">INPUTS</span></span>

### <span data-ttu-id="4c0e4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4c0e4-130">System.String</span></span>

## <span data-ttu-id="4c0e4-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c0e4-131">OUTPUTS</span></span>

### <span data-ttu-id="4c0e4-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="4c0e4-132">System.Object</span></span>

## <span data-ttu-id="4c0e4-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c0e4-133">NOTES</span></span>

## <span data-ttu-id="4c0e4-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c0e4-134">RELATED LINKS</span></span>

