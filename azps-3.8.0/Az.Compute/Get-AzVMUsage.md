---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: d22e36ad3cc4737be9c73d6b7cdc49329f904263
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940482"
---
# <span data-ttu-id="1cfe3-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="1cfe3-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="1cfe3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1cfe3-102">SYNOPSIS</span></span>
<span data-ttu-id="1cfe3-103">Obtém o uso da contagem do núcleo da máquina virtual para um local.</span><span class="sxs-lookup"><span data-stu-id="1cfe3-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="1cfe3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cfe3-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cfe3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1cfe3-105">DESCRIPTION</span></span>
<span data-ttu-id="1cfe3-106">O cmdlet **Get-AzVMUsage** Obtém o uso da contagem do núcleo da máquina virtual para um local.</span><span class="sxs-lookup"><span data-stu-id="1cfe3-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="1cfe3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1cfe3-107">EXAMPLES</span></span>

### <span data-ttu-id="1cfe3-108">Exemplo 1: obter o uso da contagem do núcleo para um local</span><span class="sxs-lookup"><span data-stu-id="1cfe3-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="1cfe3-109">Esse comando obtém o uso da contagem de núcleo da máquina virtual para os locais centrais dos EUA.</span><span class="sxs-lookup"><span data-stu-id="1cfe3-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="1cfe3-110">OS</span><span class="sxs-lookup"><span data-stu-id="1cfe3-110">PARAMETERS</span></span>

### <span data-ttu-id="1cfe3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cfe3-111">-DefaultProfile</span></span>
<span data-ttu-id="1cfe3-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1cfe3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cfe3-113">-Local</span><span class="sxs-lookup"><span data-stu-id="1cfe3-113">-Location</span></span>
<span data-ttu-id="1cfe3-114">Especifica o local para o qual esse cmdlet obtém o uso da contagem do núcleo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1cfe3-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="1cfe3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cfe3-115">CommonParameters</span></span>
<span data-ttu-id="1cfe3-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cfe3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cfe3-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cfe3-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cfe3-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1cfe3-118">INPUTS</span></span>

### <span data-ttu-id="1cfe3-119">System. String</span><span class="sxs-lookup"><span data-stu-id="1cfe3-119">System.String</span></span>

## <span data-ttu-id="1cfe3-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1cfe3-120">OUTPUTS</span></span>

### <span data-ttu-id="1cfe3-121">Microsoft. Azure. Commands. COMPUTE. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="1cfe3-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="1cfe3-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1cfe3-122">NOTES</span></span>

## <span data-ttu-id="1cfe3-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cfe3-123">RELATED LINKS</span></span>

[<span data-ttu-id="1cfe3-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1cfe3-124">Get-AzVM</span></span>](./Get-AzVM.md)


