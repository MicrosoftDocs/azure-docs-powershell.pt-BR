---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: 0996b327a0253e5f20c693fb8a3f3229597c80e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597418"
---
# <span data-ttu-id="a6334-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="a6334-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="a6334-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6334-102">SYNOPSIS</span></span>
<span data-ttu-id="a6334-103">Obtém o uso da contagem do núcleo da máquina virtual para um local.</span><span class="sxs-lookup"><span data-stu-id="a6334-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="a6334-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6334-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6334-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6334-105">DESCRIPTION</span></span>
<span data-ttu-id="a6334-106">O cmdlet **Get-AzVMUsage** Obtém o uso da contagem do núcleo da máquina virtual para um local.</span><span class="sxs-lookup"><span data-stu-id="a6334-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="a6334-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6334-107">EXAMPLES</span></span>

### <span data-ttu-id="a6334-108">Exemplo 1: obter o uso da contagem do núcleo para um local</span><span class="sxs-lookup"><span data-stu-id="a6334-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="a6334-109">Esse comando obtém o uso da contagem de núcleo da máquina virtual para os locais centrais dos EUA.</span><span class="sxs-lookup"><span data-stu-id="a6334-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="a6334-110">OS</span><span class="sxs-lookup"><span data-stu-id="a6334-110">PARAMETERS</span></span>

### <span data-ttu-id="a6334-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6334-111">-DefaultProfile</span></span>
<span data-ttu-id="a6334-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6334-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6334-113">-Local</span><span class="sxs-lookup"><span data-stu-id="a6334-113">-Location</span></span>
<span data-ttu-id="a6334-114">Especifica o local para o qual esse cmdlet obtém o uso da contagem do núcleo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a6334-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="a6334-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6334-115">CommonParameters</span></span>
<span data-ttu-id="a6334-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6334-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6334-117">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6334-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6334-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6334-118">INPUTS</span></span>

### <span data-ttu-id="a6334-119">System. String</span><span class="sxs-lookup"><span data-stu-id="a6334-119">System.String</span></span>

## <span data-ttu-id="a6334-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6334-120">OUTPUTS</span></span>

### <span data-ttu-id="a6334-121">Microsoft. Azure. Commands. COMPUTE. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="a6334-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="a6334-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6334-122">NOTES</span></span>

## <span data-ttu-id="a6334-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6334-123">RELATED LINKS</span></span>

[<span data-ttu-id="a6334-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a6334-124">Get-AzVM</span></span>](./Get-AzVM.md)


