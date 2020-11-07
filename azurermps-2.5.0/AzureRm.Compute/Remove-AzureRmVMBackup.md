---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmbackup
schema: 2.0.0
ms.openlocfilehash: 8805d5da061ef19037768b72c08145e45c8f2a9c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786132"
---
# <span data-ttu-id="0e02f-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="0e02f-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="0e02f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e02f-102">SYNOPSIS</span></span>
<span data-ttu-id="0e02f-103">Remove o backup de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0e02f-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e02f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e02f-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e02f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e02f-105">DESCRIPTION</span></span>

## <span data-ttu-id="0e02f-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e02f-106">EXAMPLES</span></span>

### <span data-ttu-id="0e02f-107">1:</span><span class="sxs-lookup"><span data-stu-id="0e02f-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="0e02f-108">OS</span><span class="sxs-lookup"><span data-stu-id="0e02f-108">PARAMETERS</span></span>

### <span data-ttu-id="0e02f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e02f-109">-DefaultProfile</span></span>
<span data-ttu-id="0e02f-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e02f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e02f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e02f-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="0e02f-112">-Marca</span><span class="sxs-lookup"><span data-stu-id="0e02f-112">-Tag</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e02f-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="0e02f-113">-VMName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e02f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e02f-114">CommonParameters</span></span>
<span data-ttu-id="0e02f-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e02f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e02f-116">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e02f-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e02f-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e02f-117">INPUTS</span></span>

### <span data-ttu-id="0e02f-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0e02f-118">None</span></span>
<span data-ttu-id="0e02f-119">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="0e02f-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e02f-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e02f-120">OUTPUTS</span></span>

### <span data-ttu-id="0e02f-121">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0e02f-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0e02f-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e02f-122">NOTES</span></span>

## <span data-ttu-id="0e02f-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e02f-123">RELATED LINKS</span></span>

