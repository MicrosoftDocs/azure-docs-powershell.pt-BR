---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 67c96d257be803e77555a7a93d8f9b1ebbbbf8c2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776885"
---
# <span data-ttu-id="e3dfc-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e3dfc-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="e3dfc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="e3dfc-103">Revoga um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="e3dfc-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="e3dfc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3dfc-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3dfc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="e3dfc-106">O cmdlet **REVOKE-AzDiskAccess** revoga um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="e3dfc-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="e3dfc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3dfc-107">EXAMPLES</span></span>

### <span data-ttu-id="e3dfc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3dfc-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="e3dfc-109">Revogue o acesso ao disco chamado ' Disk01 ' no grupo de recursos chamado ' ResourceGroup01 '</span><span class="sxs-lookup"><span data-stu-id="e3dfc-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="e3dfc-110">OS</span><span class="sxs-lookup"><span data-stu-id="e3dfc-110">PARAMETERS</span></span>

### <span data-ttu-id="e3dfc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3dfc-111">-AsJob</span></span>
<span data-ttu-id="e3dfc-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e3dfc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3dfc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3dfc-113">-DefaultProfile</span></span>
<span data-ttu-id="e3dfc-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3dfc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3dfc-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="e3dfc-115">-DiskName</span></span>
<span data-ttu-id="e3dfc-116">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="e3dfc-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="e3dfc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3dfc-117">-ResourceGroupName</span></span>
<span data-ttu-id="e3dfc-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e3dfc-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e3dfc-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e3dfc-119">-Confirm</span></span>
<span data-ttu-id="e3dfc-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3dfc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3dfc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3dfc-121">-WhatIf</span></span>
<span data-ttu-id="e3dfc-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e3dfc-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3dfc-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3dfc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3dfc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3dfc-124">CommonParameters</span></span>
<span data-ttu-id="e3dfc-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3dfc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3dfc-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3dfc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3dfc-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3dfc-127">INPUTS</span></span>

### <span data-ttu-id="e3dfc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e3dfc-128">System.String</span></span>

## <span data-ttu-id="e3dfc-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3dfc-129">OUTPUTS</span></span>

### <span data-ttu-id="e3dfc-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="e3dfc-130">System.Object</span></span>

## <span data-ttu-id="e3dfc-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3dfc-131">NOTES</span></span>

## <span data-ttu-id="e3dfc-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3dfc-132">RELATED LINKS</span></span>

