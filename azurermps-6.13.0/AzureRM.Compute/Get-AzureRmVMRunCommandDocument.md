---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
ms.openlocfilehash: 070fe50f74db08caab375a97d4d8ff6be3e970ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429581"
---
# <span data-ttu-id="88ddd-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="88ddd-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="88ddd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="88ddd-103">Obter o documento de comando executar.</span><span class="sxs-lookup"><span data-stu-id="88ddd-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88ddd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88ddd-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88ddd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88ddd-105">DESCRIPTION</span></span>
<span data-ttu-id="88ddd-106">Obter o documento de comando executar.</span><span class="sxs-lookup"><span data-stu-id="88ddd-106">Get run command document.</span></span>

## <span data-ttu-id="88ddd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88ddd-107">EXAMPLES</span></span>

### <span data-ttu-id="88ddd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="88ddd-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="88ddd-109">Obtém um documento de comando de execução específico para ' RunPowerShellScript ' em ' westus '.</span><span class="sxs-lookup"><span data-stu-id="88ddd-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>
<span data-ttu-id="88ddd-110">Get-AzureRmVMRunCommandDocument-Location $loc</span><span class="sxs-lookup"><span data-stu-id="88ddd-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="88ddd-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="88ddd-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="88ddd-112">Lista todos os comandos de execução disponíveis em ' westus '.</span><span class="sxs-lookup"><span data-stu-id="88ddd-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="88ddd-113">OS</span><span class="sxs-lookup"><span data-stu-id="88ddd-113">PARAMETERS</span></span>

### <span data-ttu-id="88ddd-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="88ddd-114">-CommandId</span></span>
<span data-ttu-id="88ddd-115">A ID do comando.</span><span class="sxs-lookup"><span data-stu-id="88ddd-115">The command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ddd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ddd-116">-DefaultProfile</span></span>
<span data-ttu-id="88ddd-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88ddd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88ddd-118">-Local</span><span class="sxs-lookup"><span data-stu-id="88ddd-118">-Location</span></span>
<span data-ttu-id="88ddd-119">O local no qual os comandos de execução são consultados.</span><span class="sxs-lookup"><span data-stu-id="88ddd-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="88ddd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ddd-120">CommonParameters</span></span>
<span data-ttu-id="88ddd-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88ddd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ddd-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88ddd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ddd-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88ddd-123">INPUTS</span></span>

### <span data-ttu-id="88ddd-124">System. String</span><span class="sxs-lookup"><span data-stu-id="88ddd-124">System.String</span></span>

## <span data-ttu-id="88ddd-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88ddd-125">OUTPUTS</span></span>

### <span data-ttu-id="88ddd-126">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="88ddd-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="88ddd-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88ddd-127">NOTES</span></span>

## <span data-ttu-id="88ddd-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88ddd-128">RELATED LINKS</span></span>
