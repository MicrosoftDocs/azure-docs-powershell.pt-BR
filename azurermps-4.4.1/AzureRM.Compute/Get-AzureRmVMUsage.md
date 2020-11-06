---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: af360334ab546685deadad45c2ea3f8954c226f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432641"
---
# <span data-ttu-id="1f521-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="1f521-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="1f521-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f521-102">SYNOPSIS</span></span>
<span data-ttu-id="1f521-103">Obtém o uso da contagem do núcleo da máquina virtual para um local.</span><span class="sxs-lookup"><span data-stu-id="1f521-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f521-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f521-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f521-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f521-105">DESCRIPTION</span></span>
<span data-ttu-id="1f521-106">O cmdlet **Get-AzureRmVMUsage** Obtém o uso da contagem do núcleo da máquina virtual para um local.</span><span class="sxs-lookup"><span data-stu-id="1f521-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="1f521-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f521-107">EXAMPLES</span></span>

### <span data-ttu-id="1f521-108">Exemplo 1: obter o uso da contagem do núcleo para um local</span><span class="sxs-lookup"><span data-stu-id="1f521-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="1f521-109">Esse comando obtém o uso da contagem de núcleo da máquina virtual para os locais centrais dos EUA.</span><span class="sxs-lookup"><span data-stu-id="1f521-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="1f521-110">OS</span><span class="sxs-lookup"><span data-stu-id="1f521-110">PARAMETERS</span></span>

### <span data-ttu-id="1f521-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f521-111">-DefaultProfile</span></span>
<span data-ttu-id="1f521-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f521-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f521-113">-Local</span><span class="sxs-lookup"><span data-stu-id="1f521-113">-Location</span></span>
<span data-ttu-id="1f521-114">Especifica o local para o qual esse cmdlet obtém o uso da contagem do núcleo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1f521-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="1f521-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f521-115">CommonParameters</span></span>
<span data-ttu-id="1f521-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f521-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f521-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f521-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f521-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f521-118">INPUTS</span></span>

## <span data-ttu-id="1f521-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f521-119">OUTPUTS</span></span>

## <span data-ttu-id="1f521-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f521-120">NOTES</span></span>

## <span data-ttu-id="1f521-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f521-121">RELATED LINKS</span></span>

[<span data-ttu-id="1f521-122">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1f521-122">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


