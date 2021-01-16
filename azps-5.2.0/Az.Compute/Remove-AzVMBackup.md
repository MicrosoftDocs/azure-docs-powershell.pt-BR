---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 85b7a873a921e7fd08055e1e3adc7c70831f8fa1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263172"
---
# <span data-ttu-id="70ba2-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="70ba2-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="70ba2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70ba2-102">SYNOPSIS</span></span>
<span data-ttu-id="70ba2-103">Remove o backup de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="70ba2-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="70ba2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70ba2-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70ba2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70ba2-105">DESCRIPTION</span></span>

## <span data-ttu-id="70ba2-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70ba2-106">EXAMPLES</span></span>

### <span data-ttu-id="70ba2-107">1:</span><span class="sxs-lookup"><span data-stu-id="70ba2-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="70ba2-108">OS</span><span class="sxs-lookup"><span data-stu-id="70ba2-108">PARAMETERS</span></span>

### <span data-ttu-id="70ba2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ba2-109">-DefaultProfile</span></span>
<span data-ttu-id="70ba2-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70ba2-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70ba2-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70ba2-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="70ba2-112">-Marca</span><span class="sxs-lookup"><span data-stu-id="70ba2-112">-Tag</span></span>
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

### <span data-ttu-id="70ba2-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="70ba2-113">-VMName</span></span>
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

### <span data-ttu-id="70ba2-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ba2-114">CommonParameters</span></span>
<span data-ttu-id="70ba2-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ba2-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ba2-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70ba2-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ba2-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70ba2-117">INPUTS</span></span>

### <span data-ttu-id="70ba2-118">System. String</span><span class="sxs-lookup"><span data-stu-id="70ba2-118">System.String</span></span>

## <span data-ttu-id="70ba2-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70ba2-119">OUTPUTS</span></span>

### <span data-ttu-id="70ba2-120">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="70ba2-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="70ba2-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70ba2-121">NOTES</span></span>

## <span data-ttu-id="70ba2-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70ba2-122">RELATED LINKS</span></span>
