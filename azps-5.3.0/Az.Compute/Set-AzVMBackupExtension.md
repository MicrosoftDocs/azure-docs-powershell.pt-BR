---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 9ead4b38575bc297a820bda61eb6faf0beaf80d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434199"
---
# <span data-ttu-id="56b0e-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="56b0e-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="56b0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="56b0e-103">Define as propriedades de extensão de backup em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="56b0e-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="56b0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56b0e-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56b0e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56b0e-105">DESCRIPTION</span></span>

## <span data-ttu-id="56b0e-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56b0e-106">EXAMPLES</span></span>

### <span data-ttu-id="56b0e-107">1:</span><span class="sxs-lookup"><span data-stu-id="56b0e-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="56b0e-108">OS</span><span class="sxs-lookup"><span data-stu-id="56b0e-108">PARAMETERS</span></span>

### <span data-ttu-id="56b0e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b0e-109">-DefaultProfile</span></span>
<span data-ttu-id="56b0e-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56b0e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56b0e-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="56b0e-111">-Name</span></span>
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

### <span data-ttu-id="56b0e-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56b0e-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="56b0e-113">-Marca</span><span class="sxs-lookup"><span data-stu-id="56b0e-113">-Tag</span></span>
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

### <span data-ttu-id="56b0e-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="56b0e-114">-VMName</span></span>
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

### <span data-ttu-id="56b0e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b0e-115">CommonParameters</span></span>
<span data-ttu-id="56b0e-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56b0e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b0e-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56b0e-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b0e-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56b0e-118">INPUTS</span></span>

### <span data-ttu-id="56b0e-119">System. String</span><span class="sxs-lookup"><span data-stu-id="56b0e-119">System.String</span></span>

## <span data-ttu-id="56b0e-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56b0e-120">OUTPUTS</span></span>

### <span data-ttu-id="56b0e-121">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="56b0e-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="56b0e-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56b0e-122">NOTES</span></span>

## <span data-ttu-id="56b0e-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56b0e-123">RELATED LINKS</span></span>
