---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 23ae31c79c33e9299d1cf3dc5998798657408da4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887897"
---
# <span data-ttu-id="8ee45-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="8ee45-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="8ee45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ee45-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee45-103">Remove o backup de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ee45-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="8ee45-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8ee45-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ee45-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8ee45-105">DESCRIPTION</span></span>

## <span data-ttu-id="8ee45-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ee45-106">EXAMPLES</span></span>

### <span data-ttu-id="8ee45-107">1:</span><span class="sxs-lookup"><span data-stu-id="8ee45-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="8ee45-108">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8ee45-108">PARAMETERS</span></span>

### <span data-ttu-id="8ee45-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee45-109">-DefaultProfile</span></span>
<span data-ttu-id="8ee45-110">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8ee45-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ee45-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee45-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="8ee45-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="8ee45-112">-Tag</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ee45-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="8ee45-113">-VMName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ee45-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee45-114">CommonParameters</span></span>
<span data-ttu-id="8ee45-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee45-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee45-116">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ee45-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee45-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ee45-117">INPUTS</span></span>

### <span data-ttu-id="8ee45-118">System.String</span><span class="sxs-lookup"><span data-stu-id="8ee45-118">System.String</span></span>

## <span data-ttu-id="8ee45-119">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8ee45-119">OUTPUTS</span></span>

### <span data-ttu-id="8ee45-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8ee45-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8ee45-121">NOTES</span><span class="sxs-lookup"><span data-stu-id="8ee45-121">NOTES</span></span>

## <span data-ttu-id="8ee45-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ee45-122">RELATED LINKS</span></span>
