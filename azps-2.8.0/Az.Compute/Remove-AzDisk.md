---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: 46cbb87d54d1eb80857d3d0fbc786cb8296f4ac0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597331"
---
# <span data-ttu-id="93212-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="93212-101">Remove-AzDisk</span></span>

## <span data-ttu-id="93212-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93212-102">SYNOPSIS</span></span>
<span data-ttu-id="93212-103">Remove um disco.</span><span class="sxs-lookup"><span data-stu-id="93212-103">Removes a disk.</span></span>

## <span data-ttu-id="93212-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93212-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93212-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93212-105">DESCRIPTION</span></span>
<span data-ttu-id="93212-106">O cmdlet **Remove-AzDisk** remove um disco.</span><span class="sxs-lookup"><span data-stu-id="93212-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="93212-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93212-107">EXAMPLES</span></span>

### <span data-ttu-id="93212-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="93212-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="93212-109">Este comando Remove o disco chamado "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="93212-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="93212-110">OS</span><span class="sxs-lookup"><span data-stu-id="93212-110">PARAMETERS</span></span>

### <span data-ttu-id="93212-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93212-111">-AsJob</span></span>
<span data-ttu-id="93212-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="93212-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="93212-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93212-113">-DefaultProfile</span></span>
<span data-ttu-id="93212-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93212-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93212-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="93212-115">-DiskName</span></span>
<span data-ttu-id="93212-116">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="93212-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="93212-117">-Force</span><span class="sxs-lookup"><span data-stu-id="93212-117">-Force</span></span>
<span data-ttu-id="93212-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="93212-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93212-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93212-119">-ResourceGroupName</span></span>
<span data-ttu-id="93212-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="93212-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="93212-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="93212-121">-Confirm</span></span>
<span data-ttu-id="93212-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93212-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93212-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93212-123">-WhatIf</span></span>
<span data-ttu-id="93212-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="93212-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93212-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="93212-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93212-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93212-126">CommonParameters</span></span>
<span data-ttu-id="93212-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93212-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93212-128">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93212-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93212-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93212-129">INPUTS</span></span>

### <span data-ttu-id="93212-130">System. String</span><span class="sxs-lookup"><span data-stu-id="93212-130">System.String</span></span>

## <span data-ttu-id="93212-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93212-131">OUTPUTS</span></span>

### <span data-ttu-id="93212-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="93212-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="93212-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93212-133">NOTES</span></span>

## <span data-ttu-id="93212-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93212-134">RELATED LINKS</span></span>
