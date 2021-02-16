---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 35e767c340d5418ae500c4cc87a4b40741d8ba6a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117834"
---
# <span data-ttu-id="34054-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="34054-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="34054-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34054-102">SYNOPSIS</span></span>
<span data-ttu-id="34054-103">Revoga um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="34054-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="34054-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34054-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34054-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="34054-105">DESCRIPTION</span></span>
<span data-ttu-id="34054-106">O **cmdlet Revoke-AzSnapshotAccess** revoga um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="34054-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="34054-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="34054-107">EXAMPLES</span></span>

### <span data-ttu-id="34054-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="34054-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="34054-109">Revogar o acesso ao instantâneo chamado "Instantâneo01" no grupo de recursos chamado 'ResourceGroup01'</span><span class="sxs-lookup"><span data-stu-id="34054-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="34054-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34054-110">PARAMETERS</span></span>

### <span data-ttu-id="34054-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34054-111">-AsJob</span></span>
<span data-ttu-id="34054-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="34054-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34054-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34054-113">-DefaultProfile</span></span>
<span data-ttu-id="34054-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="34054-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34054-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34054-115">-ResourceGroupName</span></span>
<span data-ttu-id="34054-116">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="34054-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="34054-117">-Nomedo Instantâneo</span><span class="sxs-lookup"><span data-stu-id="34054-117">-SnapshotName</span></span>
<span data-ttu-id="34054-118">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="34054-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="34054-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="34054-119">-Confirm</span></span>
<span data-ttu-id="34054-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34054-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34054-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34054-121">-WhatIf</span></span>
<span data-ttu-id="34054-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="34054-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34054-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34054-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34054-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34054-124">CommonParameters</span></span>
<span data-ttu-id="34054-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34054-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34054-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34054-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34054-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="34054-127">INPUTS</span></span>

### <span data-ttu-id="34054-128">System.String</span><span class="sxs-lookup"><span data-stu-id="34054-128">System.String</span></span>

## <span data-ttu-id="34054-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="34054-129">OUTPUTS</span></span>

### <span data-ttu-id="34054-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="34054-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="34054-131">Notas</span><span class="sxs-lookup"><span data-stu-id="34054-131">NOTES</span></span>

## <span data-ttu-id="34054-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34054-132">RELATED LINKS</span></span>
