---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: edd2d89cfe0488021ef62780ade80cb2b98437c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427268"
---
# <span data-ttu-id="c520d-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="c520d-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="c520d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c520d-102">SYNOPSIS</span></span>
<span data-ttu-id="c520d-103">Remove um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="c520d-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c520d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c520d-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c520d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c520d-105">DESCRIPTION</span></span>
<span data-ttu-id="c520d-106">O cmdlet **Remove-AzureRmSnapshot** remove um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="c520d-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="c520d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c520d-107">EXAMPLES</span></span>

### <span data-ttu-id="c520d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c520d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="c520d-109">Este comando Remove o instantâneo chamado "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c520d-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c520d-110">OS</span><span class="sxs-lookup"><span data-stu-id="c520d-110">PARAMETERS</span></span>

### <span data-ttu-id="c520d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c520d-111">-AsJob</span></span>
<span data-ttu-id="c520d-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="c520d-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c520d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c520d-113">-DefaultProfile</span></span>
<span data-ttu-id="c520d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c520d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c520d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c520d-115">-Force</span></span>
<span data-ttu-id="c520d-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c520d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c520d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c520d-117">-ResourceGroupName</span></span>
<span data-ttu-id="c520d-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c520d-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c520d-119">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="c520d-119">-SnapshotName</span></span>
<span data-ttu-id="c520d-120">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="c520d-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="c520d-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c520d-121">-Confirm</span></span>
<span data-ttu-id="c520d-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c520d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c520d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c520d-123">-WhatIf</span></span>
<span data-ttu-id="c520d-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c520d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c520d-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c520d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c520d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c520d-126">CommonParameters</span></span>
<span data-ttu-id="c520d-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c520d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c520d-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c520d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c520d-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c520d-129">INPUTS</span></span>

### <span data-ttu-id="c520d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c520d-130">System.String</span></span>

## <span data-ttu-id="c520d-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c520d-131">OUTPUTS</span></span>

### <span data-ttu-id="c520d-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c520d-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c520d-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c520d-133">NOTES</span></span>

## <span data-ttu-id="c520d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c520d-134">RELATED LINKS</span></span>
