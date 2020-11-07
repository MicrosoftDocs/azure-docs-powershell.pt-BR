---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbackupextension
schema: 2.0.0
ms.openlocfilehash: 5d31ad189dcc5337b81373d52a026e01f93f08a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785948"
---
# <span data-ttu-id="8c24a-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="8c24a-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="8c24a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c24a-102">SYNOPSIS</span></span>
<span data-ttu-id="8c24a-103">Define as propriedades de extensão de backup em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8c24a-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c24a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c24a-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c24a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c24a-105">DESCRIPTION</span></span>

## <span data-ttu-id="8c24a-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c24a-106">EXAMPLES</span></span>

### <span data-ttu-id="8c24a-107">1:</span><span class="sxs-lookup"><span data-stu-id="8c24a-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="8c24a-108">OS</span><span class="sxs-lookup"><span data-stu-id="8c24a-108">PARAMETERS</span></span>

### <span data-ttu-id="8c24a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c24a-109">-DefaultProfile</span></span>
<span data-ttu-id="8c24a-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c24a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c24a-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c24a-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c24a-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c24a-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="8c24a-113">-Marca</span><span class="sxs-lookup"><span data-stu-id="8c24a-113">-Tag</span></span>
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

### <span data-ttu-id="8c24a-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="8c24a-114">-VMName</span></span>
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

### <span data-ttu-id="8c24a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c24a-115">CommonParameters</span></span>
<span data-ttu-id="8c24a-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c24a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c24a-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c24a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c24a-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c24a-118">INPUTS</span></span>

### <span data-ttu-id="8c24a-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8c24a-119">None</span></span>
<span data-ttu-id="8c24a-120">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8c24a-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c24a-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c24a-121">OUTPUTS</span></span>

### <span data-ttu-id="8c24a-122">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8c24a-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8c24a-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c24a-123">NOTES</span></span>

## <span data-ttu-id="8c24a-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c24a-124">RELATED LINKS</span></span>

