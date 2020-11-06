---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
ms.openlocfilehash: fd52bf58e3e240f65be88d8f9f682b2543e1f458
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611137"
---
# <span data-ttu-id="e3bdd-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="e3bdd-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="e3bdd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="e3bdd-103">Obter o documento de comando executar.</span><span class="sxs-lookup"><span data-stu-id="e3bdd-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3bdd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3bdd-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3bdd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3bdd-105">DESCRIPTION</span></span>
<span data-ttu-id="e3bdd-106">Obter o documento de comando executar.</span><span class="sxs-lookup"><span data-stu-id="e3bdd-106">Get run command document.</span></span>

## <span data-ttu-id="e3bdd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3bdd-107">EXAMPLES</span></span>

### <span data-ttu-id="e3bdd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3bdd-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="e3bdd-109">Obtém um documento de comando de execução específico para ' RunPowerShellScript ' em ' westus '.</span><span class="sxs-lookup"><span data-stu-id="e3bdd-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="e3bdd-110">Get-AzureRmVMRunCommandDocument-Location $loc</span><span class="sxs-lookup"><span data-stu-id="e3bdd-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="e3bdd-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e3bdd-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="e3bdd-112">Lista todos os comandos de execução disponíveis em ' westus '.</span><span class="sxs-lookup"><span data-stu-id="e3bdd-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="e3bdd-113">OS</span><span class="sxs-lookup"><span data-stu-id="e3bdd-113">PARAMETERS</span></span>

### <span data-ttu-id="e3bdd-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="e3bdd-114">-CommandId</span></span>
<span data-ttu-id="e3bdd-115">A ID do comando.</span><span class="sxs-lookup"><span data-stu-id="e3bdd-115">The command id.</span></span>

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

### <span data-ttu-id="e3bdd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3bdd-116">-DefaultProfile</span></span>
<span data-ttu-id="e3bdd-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3bdd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3bdd-118">-Local</span><span class="sxs-lookup"><span data-stu-id="e3bdd-118">-Location</span></span>
<span data-ttu-id="e3bdd-119">O local no qual os comandos de execução são consultados.</span><span class="sxs-lookup"><span data-stu-id="e3bdd-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="e3bdd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3bdd-120">CommonParameters</span></span>
<span data-ttu-id="e3bdd-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3bdd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3bdd-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3bdd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3bdd-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3bdd-123">INPUTS</span></span>

### <span data-ttu-id="e3bdd-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e3bdd-124">System.String</span></span>

## <span data-ttu-id="e3bdd-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3bdd-125">OUTPUTS</span></span>

### <span data-ttu-id="e3bdd-126">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="e3bdd-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="e3bdd-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3bdd-127">NOTES</span></span>

## <span data-ttu-id="e3bdd-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3bdd-128">RELATED LINKS</span></span>

