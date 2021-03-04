---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 7be9116814af3f11e6bd61668b77df133676ab1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893364"
---
# <span data-ttu-id="5d223-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="5d223-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="5d223-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d223-102">SYNOPSIS</span></span>
<span data-ttu-id="5d223-103">Define as propriedades de extensão de backup em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5d223-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="5d223-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5d223-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d223-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5d223-105">DESCRIPTION</span></span>

## <span data-ttu-id="5d223-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d223-106">EXAMPLES</span></span>

### <span data-ttu-id="5d223-107">1:</span><span class="sxs-lookup"><span data-stu-id="5d223-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="5d223-108">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5d223-108">PARAMETERS</span></span>

### <span data-ttu-id="5d223-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d223-109">-DefaultProfile</span></span>
<span data-ttu-id="5d223-110">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5d223-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d223-111">-Name</span><span class="sxs-lookup"><span data-stu-id="5d223-111">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d223-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d223-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="5d223-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="5d223-113">-Tag</span></span>
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

### <span data-ttu-id="5d223-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="5d223-114">-VMName</span></span>
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

### <span data-ttu-id="5d223-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d223-115">CommonParameters</span></span>
<span data-ttu-id="5d223-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d223-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d223-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d223-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d223-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d223-118">INPUTS</span></span>

### <span data-ttu-id="5d223-119">System.String</span><span class="sxs-lookup"><span data-stu-id="5d223-119">System.String</span></span>

## <span data-ttu-id="5d223-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5d223-120">OUTPUTS</span></span>

### <span data-ttu-id="5d223-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5d223-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5d223-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="5d223-122">NOTES</span></span>

## <span data-ttu-id="5d223-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d223-123">RELATED LINKS</span></span>
