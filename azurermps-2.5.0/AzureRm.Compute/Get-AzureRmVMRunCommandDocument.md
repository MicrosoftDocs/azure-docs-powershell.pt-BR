---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmruncommanddocument
schema: 2.0.0
ms.openlocfilehash: d51528cab51e4e6fe6cda428e25965d65c449c4b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786178"
---
# <span data-ttu-id="4a061-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="4a061-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="4a061-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a061-102">SYNOPSIS</span></span>
<span data-ttu-id="4a061-103">Obter o documento de comando executar.</span><span class="sxs-lookup"><span data-stu-id="4a061-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a061-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a061-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a061-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a061-105">DESCRIPTION</span></span>
<span data-ttu-id="4a061-106">Obter o documento de comando executar.</span><span class="sxs-lookup"><span data-stu-id="4a061-106">Get run command document.</span></span>

## <span data-ttu-id="4a061-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a061-107">EXAMPLES</span></span>

### <span data-ttu-id="4a061-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4a061-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="4a061-109">Obtém um documento de comando de execução específico para ' RunPowerShellScript ' em ' westus '.</span><span class="sxs-lookup"><span data-stu-id="4a061-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="4a061-110">Get-AzureRmVMRunCommandDocument-Location $loc</span><span class="sxs-lookup"><span data-stu-id="4a061-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="4a061-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4a061-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="4a061-112">Lista todos os comandos de execução disponíveis em ' westus '.</span><span class="sxs-lookup"><span data-stu-id="4a061-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="4a061-113">OS</span><span class="sxs-lookup"><span data-stu-id="4a061-113">PARAMETERS</span></span>

### <span data-ttu-id="4a061-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="4a061-114">-CommandId</span></span>
<span data-ttu-id="4a061-115">A ID do comando.</span><span class="sxs-lookup"><span data-stu-id="4a061-115">The command id.</span></span>

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

### <span data-ttu-id="4a061-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a061-116">-DefaultProfile</span></span>
<span data-ttu-id="4a061-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a061-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a061-118">-Local</span><span class="sxs-lookup"><span data-stu-id="4a061-118">-Location</span></span>
<span data-ttu-id="4a061-119">O local no qual os comandos de execução são consultados.</span><span class="sxs-lookup"><span data-stu-id="4a061-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="4a061-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a061-120">CommonParameters</span></span>
<span data-ttu-id="4a061-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a061-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a061-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a061-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a061-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a061-123">INPUTS</span></span>

### <span data-ttu-id="4a061-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4a061-124">System.String</span></span>

## <span data-ttu-id="4a061-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a061-125">OUTPUTS</span></span>

### <span data-ttu-id="4a061-126">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="4a061-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="4a061-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a061-127">NOTES</span></span>

## <span data-ttu-id="4a061-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a061-128">RELATED LINKS</span></span>

