---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: 9ec94d0c11bf9302156355c28566ce16f48ae148
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430519"
---
# <span data-ttu-id="65576-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="65576-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="65576-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65576-102">SYNOPSIS</span></span>
<span data-ttu-id="65576-103">Obtém o status de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="65576-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65576-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65576-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="65576-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65576-105">DESCRIPTION</span></span>
<span data-ttu-id="65576-106">O cmdlet **Get-AzureRmVMDiskEncryptionStatus** Obtém o status de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="65576-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="65576-107">Ele exibe o status de criptografia do sistema operacional e dos volumes de dados.</span><span class="sxs-lookup"><span data-stu-id="65576-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="65576-108">Além do status de criptografia, ele também exibe a URL de segredo de criptografia, a URL da chave de criptografia de chave, as IDs de recurso dos **cofres** de chaves onde a chave de criptografia e a chave de criptografia de chave do volume do sistema operacional estão presentes.</span><span class="sxs-lookup"><span data-stu-id="65576-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="65576-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65576-109">EXAMPLES</span></span>

### <span data-ttu-id="65576-110">Exemplo 1: obter o status de criptografia de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="65576-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="65576-111">Esse comando obtém o status de criptografia da máquina virtual chamada VM001.</span><span class="sxs-lookup"><span data-stu-id="65576-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="65576-112">OS</span><span class="sxs-lookup"><span data-stu-id="65576-112">PARAMETERS</span></span>

### <span data-ttu-id="65576-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="65576-113">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65576-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65576-114">-ResourceGroupName</span></span>
<span data-ttu-id="65576-115">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="65576-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="65576-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="65576-116">-VMName</span></span>
<span data-ttu-id="65576-117">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="65576-117">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="65576-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65576-118">CommonParameters</span></span>
<span data-ttu-id="65576-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65576-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65576-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65576-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65576-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65576-121">INPUTS</span></span>

### <span data-ttu-id="65576-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="65576-122">None</span></span>
<span data-ttu-id="65576-123">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="65576-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="65576-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65576-124">OUTPUTS</span></span>

## <span data-ttu-id="65576-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65576-125">NOTES</span></span>

## <span data-ttu-id="65576-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65576-126">RELATED LINKS</span></span>

[<span data-ttu-id="65576-127">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="65576-127">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="65576-128">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="65576-128">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


