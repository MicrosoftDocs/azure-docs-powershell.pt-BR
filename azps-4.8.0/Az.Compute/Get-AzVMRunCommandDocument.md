---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 5aeb8d7ba44f07519ff3cdfdc5e775687bd98260
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948129"
---
# <span data-ttu-id="ea72c-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="ea72c-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="ea72c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea72c-102">SYNOPSIS</span></span>
<span data-ttu-id="ea72c-103">Obter um documento de comando executar.</span><span class="sxs-lookup"><span data-stu-id="ea72c-103">Get a run command document.</span></span>

## <span data-ttu-id="ea72c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea72c-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea72c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea72c-105">DESCRIPTION</span></span>
<span data-ttu-id="ea72c-106">Obter um documento de comando executar.</span><span class="sxs-lookup"><span data-stu-id="ea72c-106">Get a run command document.</span></span>

## <span data-ttu-id="ea72c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea72c-107">EXAMPLES</span></span>

### <span data-ttu-id="ea72c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea72c-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="ea72c-109">Obtém um documento de comando de execução específico para ' RunPowerShellScript ' em ' westus '.</span><span class="sxs-lookup"><span data-stu-id="ea72c-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="ea72c-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ea72c-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="ea72c-111">Lista todos os comandos de execução disponíveis em ' westus '.</span><span class="sxs-lookup"><span data-stu-id="ea72c-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="ea72c-112">OS</span><span class="sxs-lookup"><span data-stu-id="ea72c-112">PARAMETERS</span></span>

### <span data-ttu-id="ea72c-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="ea72c-113">-CommandId</span></span>
<span data-ttu-id="ea72c-114">A ID do comando.</span><span class="sxs-lookup"><span data-stu-id="ea72c-114">The command ID.</span></span>

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

### <span data-ttu-id="ea72c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea72c-115">-DefaultProfile</span></span>
<span data-ttu-id="ea72c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea72c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea72c-117">-Local</span><span class="sxs-lookup"><span data-stu-id="ea72c-117">-Location</span></span>
<span data-ttu-id="ea72c-118">O local no qual os comandos de execução são consultados.</span><span class="sxs-lookup"><span data-stu-id="ea72c-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="ea72c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea72c-119">CommonParameters</span></span>
<span data-ttu-id="ea72c-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea72c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea72c-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea72c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea72c-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea72c-122">INPUTS</span></span>

### <span data-ttu-id="ea72c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ea72c-123">System.String</span></span>

## <span data-ttu-id="ea72c-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea72c-124">OUTPUTS</span></span>

### <span data-ttu-id="ea72c-125">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="ea72c-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="ea72c-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea72c-126">NOTES</span></span>

## <span data-ttu-id="ea72c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea72c-127">RELATED LINKS</span></span>
