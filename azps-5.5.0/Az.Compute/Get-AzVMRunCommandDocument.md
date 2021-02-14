---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 5aeb8d7ba44f07519ff3cdfdc5e775687bd98260
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116538"
---
# <span data-ttu-id="d6275-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="d6275-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="d6275-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6275-102">SYNOPSIS</span></span>
<span data-ttu-id="d6275-103">Obter um documento de comando executar.</span><span class="sxs-lookup"><span data-stu-id="d6275-103">Get a run command document.</span></span>

## <span data-ttu-id="d6275-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6275-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6275-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6275-105">DESCRIPTION</span></span>
<span data-ttu-id="d6275-106">Obter um documento de comando executar.</span><span class="sxs-lookup"><span data-stu-id="d6275-106">Get a run command document.</span></span>

## <span data-ttu-id="d6275-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d6275-107">EXAMPLES</span></span>

### <span data-ttu-id="d6275-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d6275-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="d6275-109">Obtém um documento de comando de executar específico para 'RunPowerShellScript' em 'westus'.</span><span class="sxs-lookup"><span data-stu-id="d6275-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="d6275-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d6275-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="d6275-111">Lista todos os comandos de executar disponíveis em 'westus'.</span><span class="sxs-lookup"><span data-stu-id="d6275-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="d6275-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6275-112">PARAMETERS</span></span>

### <span data-ttu-id="d6275-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="d6275-113">-CommandId</span></span>
<span data-ttu-id="d6275-114">A ID do comando.</span><span class="sxs-lookup"><span data-stu-id="d6275-114">The command ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6275-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6275-115">-DefaultProfile</span></span>
<span data-ttu-id="d6275-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d6275-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6275-117">-Local</span><span class="sxs-lookup"><span data-stu-id="d6275-117">-Location</span></span>
<span data-ttu-id="d6275-118">O local no qual os comandos de executar são consultados.</span><span class="sxs-lookup"><span data-stu-id="d6275-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="d6275-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6275-119">CommonParameters</span></span>
<span data-ttu-id="d6275-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6275-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6275-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6275-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6275-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="d6275-122">INPUTS</span></span>

### <span data-ttu-id="d6275-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d6275-123">System.String</span></span>

## <span data-ttu-id="d6275-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="d6275-124">OUTPUTS</span></span>

### <span data-ttu-id="d6275-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="d6275-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="d6275-126">Notas</span><span class="sxs-lookup"><span data-stu-id="d6275-126">NOTES</span></span>

## <span data-ttu-id="d6275-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6275-127">RELATED LINKS</span></span>
