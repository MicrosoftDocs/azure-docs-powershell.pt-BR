---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 02040fcb80fbf020b9d9dd3725369e75fbbf15c8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776921"
---
# <span data-ttu-id="1f244-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="1f244-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="1f244-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f244-102">SYNOPSIS</span></span>
<span data-ttu-id="1f244-103">Remove o backup de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1f244-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="1f244-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f244-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f244-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f244-105">DESCRIPTION</span></span>

## <span data-ttu-id="1f244-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f244-106">EXAMPLES</span></span>

### <span data-ttu-id="1f244-107">1:</span><span class="sxs-lookup"><span data-stu-id="1f244-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="1f244-108">OS</span><span class="sxs-lookup"><span data-stu-id="1f244-108">PARAMETERS</span></span>

### <span data-ttu-id="1f244-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f244-109">-DefaultProfile</span></span>
<span data-ttu-id="1f244-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f244-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f244-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f244-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="1f244-112">-Marca</span><span class="sxs-lookup"><span data-stu-id="1f244-112">-Tag</span></span>
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

### <span data-ttu-id="1f244-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="1f244-113">-VMName</span></span>
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

### <span data-ttu-id="1f244-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f244-114">CommonParameters</span></span>
<span data-ttu-id="1f244-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f244-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f244-116">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f244-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f244-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f244-117">INPUTS</span></span>

### <span data-ttu-id="1f244-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1f244-118">None</span></span>
<span data-ttu-id="1f244-119">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1f244-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f244-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f244-120">OUTPUTS</span></span>

### <span data-ttu-id="1f244-121">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1f244-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1f244-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f244-122">NOTES</span></span>

## <span data-ttu-id="1f244-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f244-123">RELATED LINKS</span></span>

