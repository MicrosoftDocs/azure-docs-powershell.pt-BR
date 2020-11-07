---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
ms.openlocfilehash: 210c66f91836b40c719d91907fc78bd907d0fe86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786570"
---
# <span data-ttu-id="efa4e-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="efa4e-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="efa4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="efa4e-102">SYNOPSIS</span></span>
<span data-ttu-id="efa4e-103">Obtém o uso da contagem do núcleo da máquina virtual para um local.</span><span class="sxs-lookup"><span data-stu-id="efa4e-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efa4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efa4e-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efa4e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="efa4e-105">DESCRIPTION</span></span>
<span data-ttu-id="efa4e-106">O cmdlet **Get-AzureRmVMUsage** Obtém o uso da contagem do núcleo da máquina virtual para um local.</span><span class="sxs-lookup"><span data-stu-id="efa4e-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="efa4e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="efa4e-107">EXAMPLES</span></span>

### <span data-ttu-id="efa4e-108">Exemplo 1: obter o uso da contagem do núcleo para um local</span><span class="sxs-lookup"><span data-stu-id="efa4e-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="efa4e-109">Esse comando obtém o uso da contagem de núcleo da máquina virtual para os locais centrais dos EUA.</span><span class="sxs-lookup"><span data-stu-id="efa4e-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="efa4e-110">OS</span><span class="sxs-lookup"><span data-stu-id="efa4e-110">PARAMETERS</span></span>

### <span data-ttu-id="efa4e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa4e-111">-DefaultProfile</span></span>
<span data-ttu-id="efa4e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="efa4e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efa4e-113">-Local</span><span class="sxs-lookup"><span data-stu-id="efa4e-113">-Location</span></span>
<span data-ttu-id="efa4e-114">Especifica o local para o qual esse cmdlet obtém o uso da contagem do núcleo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="efa4e-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa4e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa4e-115">CommonParameters</span></span>
<span data-ttu-id="efa4e-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efa4e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa4e-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efa4e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa4e-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="efa4e-118">INPUTS</span></span>

### <span data-ttu-id="efa4e-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="efa4e-119">None</span></span>
<span data-ttu-id="efa4e-120">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="efa4e-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="efa4e-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="efa4e-121">OUTPUTS</span></span>

### <span data-ttu-id="efa4e-122">Microsoft. Azure. Commands. COMPUTE. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="efa4e-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="efa4e-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="efa4e-123">NOTES</span></span>

## <span data-ttu-id="efa4e-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efa4e-124">RELATED LINKS</span></span>

[<span data-ttu-id="efa4e-125">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="efa4e-125">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


