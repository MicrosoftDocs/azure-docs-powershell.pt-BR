---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: ef13cdfc9a137790c0d9aa842a0ba31841baa99b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893368"
---
# <span data-ttu-id="d2253-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="d2253-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="d2253-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2253-102">SYNOPSIS</span></span>
<span data-ttu-id="d2253-103">Obtém o uso da contagem principal da máquina virtual para um local.</span><span class="sxs-lookup"><span data-stu-id="d2253-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="d2253-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d2253-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2253-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d2253-105">DESCRIPTION</span></span>
<span data-ttu-id="d2253-106">O cmdlet **Get-AzVMUsage** obtém o uso da contagem principal da máquina virtual para um local.</span><span class="sxs-lookup"><span data-stu-id="d2253-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="d2253-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2253-107">EXAMPLES</span></span>

### <span data-ttu-id="d2253-108">Exemplo 1: Obter o uso de contagem principal para um local</span><span class="sxs-lookup"><span data-stu-id="d2253-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="d2253-109">Este comando obtém o uso da contagem de núcleos da máquina virtual para o local central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="d2253-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="d2253-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d2253-110">PARAMETERS</span></span>

### <span data-ttu-id="d2253-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2253-111">-DefaultProfile</span></span>
<span data-ttu-id="d2253-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d2253-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2253-113">-Location</span><span class="sxs-lookup"><span data-stu-id="d2253-113">-Location</span></span>
<span data-ttu-id="d2253-114">Especifica o local para o qual este cmdlet obtém o uso da contagem de núcleos de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d2253-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="d2253-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2253-115">CommonParameters</span></span>
<span data-ttu-id="d2253-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2253-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2253-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2253-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2253-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2253-118">INPUTS</span></span>

### <span data-ttu-id="d2253-119">System.String</span><span class="sxs-lookup"><span data-stu-id="d2253-119">System.String</span></span>

## <span data-ttu-id="d2253-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d2253-120">OUTPUTS</span></span>

### <span data-ttu-id="d2253-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="d2253-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="d2253-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="d2253-122">NOTES</span></span>

## <span data-ttu-id="d2253-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2253-123">RELATED LINKS</span></span>

[<span data-ttu-id="d2253-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d2253-124">Get-AzVM</span></span>](./Get-AzVM.md)


