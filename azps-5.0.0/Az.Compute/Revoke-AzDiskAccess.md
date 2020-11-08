---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 76fb2e7483bb510d5eceb92b51f7e5e538c3b22b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115604"
---
# <span data-ttu-id="3079d-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="3079d-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="3079d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3079d-102">SYNOPSIS</span></span>
<span data-ttu-id="3079d-103">Revoga um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="3079d-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="3079d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3079d-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3079d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3079d-105">DESCRIPTION</span></span>
<span data-ttu-id="3079d-106">O cmdlet **REVOKE-AzDiskAccess** revoga um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="3079d-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="3079d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3079d-107">EXAMPLES</span></span>

### <span data-ttu-id="3079d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3079d-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="3079d-109">Revogue o acesso ao disco chamado ' Disk01 ' no grupo de recursos chamado ' ResourceGroup01 '</span><span class="sxs-lookup"><span data-stu-id="3079d-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="3079d-110">OS</span><span class="sxs-lookup"><span data-stu-id="3079d-110">PARAMETERS</span></span>

### <span data-ttu-id="3079d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3079d-111">-AsJob</span></span>
<span data-ttu-id="3079d-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3079d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3079d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3079d-113">-DefaultProfile</span></span>
<span data-ttu-id="3079d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3079d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3079d-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="3079d-115">-DiskName</span></span>
<span data-ttu-id="3079d-116">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="3079d-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="3079d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3079d-117">-ResourceGroupName</span></span>
<span data-ttu-id="3079d-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3079d-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3079d-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3079d-119">-Confirm</span></span>
<span data-ttu-id="3079d-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3079d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3079d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3079d-121">-WhatIf</span></span>
<span data-ttu-id="3079d-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3079d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3079d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3079d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3079d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3079d-124">CommonParameters</span></span>
<span data-ttu-id="3079d-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3079d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3079d-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3079d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3079d-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3079d-127">INPUTS</span></span>

### <span data-ttu-id="3079d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3079d-128">System.String</span></span>

## <span data-ttu-id="3079d-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3079d-129">OUTPUTS</span></span>

### <span data-ttu-id="3079d-130">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3079d-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3079d-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3079d-131">NOTES</span></span>

## <span data-ttu-id="3079d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3079d-132">RELATED LINKS</span></span>
