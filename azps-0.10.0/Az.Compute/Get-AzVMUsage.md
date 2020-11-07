---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: 66a74ed2fa389c0dd39fa9fc86570ff8d68dc1dc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777000"
---
# <span data-ttu-id="d6170-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="d6170-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="d6170-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6170-102">SYNOPSIS</span></span>
<span data-ttu-id="d6170-103">Obtém o uso da contagem do núcleo da máquina virtual para um local.</span><span class="sxs-lookup"><span data-stu-id="d6170-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="d6170-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6170-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6170-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6170-105">DESCRIPTION</span></span>
<span data-ttu-id="d6170-106">O cmdlet **Get-AzVMUsage** Obtém o uso da contagem do núcleo da máquina virtual para um local.</span><span class="sxs-lookup"><span data-stu-id="d6170-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="d6170-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6170-107">EXAMPLES</span></span>

### <span data-ttu-id="d6170-108">Exemplo 1: obter o uso da contagem do núcleo para um local</span><span class="sxs-lookup"><span data-stu-id="d6170-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="d6170-109">Esse comando obtém o uso da contagem de núcleo da máquina virtual para os locais centrais dos EUA.</span><span class="sxs-lookup"><span data-stu-id="d6170-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="d6170-110">OS</span><span class="sxs-lookup"><span data-stu-id="d6170-110">PARAMETERS</span></span>

### <span data-ttu-id="d6170-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6170-111">-DefaultProfile</span></span>
<span data-ttu-id="d6170-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6170-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6170-113">-Local</span><span class="sxs-lookup"><span data-stu-id="d6170-113">-Location</span></span>
<span data-ttu-id="d6170-114">Especifica o local para o qual esse cmdlet obtém o uso da contagem do núcleo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d6170-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="d6170-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6170-115">CommonParameters</span></span>
<span data-ttu-id="d6170-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6170-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6170-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6170-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6170-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6170-118">INPUTS</span></span>

### <span data-ttu-id="d6170-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d6170-119">None</span></span>
<span data-ttu-id="d6170-120">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d6170-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d6170-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6170-121">OUTPUTS</span></span>

### <span data-ttu-id="d6170-122">Microsoft. Azure. Commands. COMPUTE. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="d6170-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="d6170-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6170-123">NOTES</span></span>

## <span data-ttu-id="d6170-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6170-124">RELATED LINKS</span></span>

[<span data-ttu-id="d6170-125">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d6170-125">Get-AzVM</span></span>](./Get-AzVM.md)


