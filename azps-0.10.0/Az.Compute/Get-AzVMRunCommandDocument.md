---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 45d051e5fc2fe750f58dc6400a037960b7eb9c7c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777008"
---
# <span data-ttu-id="738c7-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="738c7-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="738c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="738c7-102">SYNOPSIS</span></span>
<span data-ttu-id="738c7-103">Obter o documento de comando executar.</span><span class="sxs-lookup"><span data-stu-id="738c7-103">Get run command document.</span></span>

## <span data-ttu-id="738c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="738c7-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="738c7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="738c7-105">DESCRIPTION</span></span>
<span data-ttu-id="738c7-106">Obter o documento de comando executar.</span><span class="sxs-lookup"><span data-stu-id="738c7-106">Get run command document.</span></span>

## <span data-ttu-id="738c7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="738c7-107">EXAMPLES</span></span>

### <span data-ttu-id="738c7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="738c7-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="738c7-109">Obtém um documento de comando de execução específico para ' RunPowerShellScript ' em ' westus '.</span><span class="sxs-lookup"><span data-stu-id="738c7-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="738c7-110">Get-AzVMRunCommandDocument-Location $loc</span><span class="sxs-lookup"><span data-stu-id="738c7-110">Get-AzVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="738c7-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="738c7-111">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="738c7-112">Lista todos os comandos de execução disponíveis em ' westus '.</span><span class="sxs-lookup"><span data-stu-id="738c7-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="738c7-113">OS</span><span class="sxs-lookup"><span data-stu-id="738c7-113">PARAMETERS</span></span>

### <span data-ttu-id="738c7-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="738c7-114">-CommandId</span></span>
<span data-ttu-id="738c7-115">A ID do comando.</span><span class="sxs-lookup"><span data-stu-id="738c7-115">The command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="738c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="738c7-116">-DefaultProfile</span></span>
<span data-ttu-id="738c7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="738c7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="738c7-118">-Local</span><span class="sxs-lookup"><span data-stu-id="738c7-118">-Location</span></span>
<span data-ttu-id="738c7-119">O local no qual os comandos de execução são consultados.</span><span class="sxs-lookup"><span data-stu-id="738c7-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="738c7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="738c7-120">CommonParameters</span></span>
<span data-ttu-id="738c7-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="738c7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="738c7-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="738c7-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="738c7-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="738c7-123">INPUTS</span></span>

### <span data-ttu-id="738c7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="738c7-124">System.String</span></span>

## <span data-ttu-id="738c7-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="738c7-125">OUTPUTS</span></span>

### <span data-ttu-id="738c7-126">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="738c7-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="738c7-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="738c7-127">NOTES</span></span>

## <span data-ttu-id="738c7-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="738c7-128">RELATED LINKS</span></span>

