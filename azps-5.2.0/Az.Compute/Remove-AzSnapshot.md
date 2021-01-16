---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 686f7dbe4bba17017e1920dd2c67a05c2ccd5eae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263492"
---
# <span data-ttu-id="5bf3b-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="5bf3b-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="5bf3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5bf3b-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf3b-103">Remove um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="5bf3b-103">Removes a snapshot.</span></span>

## <span data-ttu-id="5bf3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5bf3b-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bf3b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5bf3b-105">DESCRIPTION</span></span>
<span data-ttu-id="5bf3b-106">O cmdlet **Remove-AzSnapshot** remove um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="5bf3b-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="5bf3b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5bf3b-107">EXAMPLES</span></span>

### <span data-ttu-id="5bf3b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5bf3b-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="5bf3b-109">Este comando Remove o instantâneo chamado "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5bf3b-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5bf3b-110">OS</span><span class="sxs-lookup"><span data-stu-id="5bf3b-110">PARAMETERS</span></span>

### <span data-ttu-id="5bf3b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5bf3b-111">-AsJob</span></span>
<span data-ttu-id="5bf3b-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="5bf3b-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5bf3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf3b-113">-DefaultProfile</span></span>
<span data-ttu-id="5bf3b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5bf3b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bf3b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5bf3b-115">-Force</span></span>
<span data-ttu-id="5bf3b-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5bf3b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5bf3b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bf3b-117">-ResourceGroupName</span></span>
<span data-ttu-id="5bf3b-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5bf3b-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5bf3b-119">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="5bf3b-119">-SnapshotName</span></span>
<span data-ttu-id="5bf3b-120">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="5bf3b-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="5bf3b-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5bf3b-121">-Confirm</span></span>
<span data-ttu-id="5bf3b-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf3b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bf3b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf3b-123">-WhatIf</span></span>
<span data-ttu-id="5bf3b-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5bf3b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bf3b-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5bf3b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bf3b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf3b-126">CommonParameters</span></span>
<span data-ttu-id="5bf3b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf3b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf3b-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bf3b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf3b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5bf3b-129">INPUTS</span></span>

### <span data-ttu-id="5bf3b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5bf3b-130">System.String</span></span>

## <span data-ttu-id="5bf3b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5bf3b-131">OUTPUTS</span></span>

### <span data-ttu-id="5bf3b-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="5bf3b-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="5bf3b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5bf3b-133">NOTES</span></span>

## <span data-ttu-id="5bf3b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bf3b-134">RELATED LINKS</span></span>
