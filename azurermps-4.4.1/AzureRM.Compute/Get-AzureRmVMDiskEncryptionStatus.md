---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: 0d7312d7ecbddf15530438e9729e470bd202e488
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603400"
---
# <span data-ttu-id="1ac32-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="1ac32-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="1ac32-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ac32-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac32-103">Obtém o status de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1ac32-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ac32-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ac32-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ac32-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ac32-105">DESCRIPTION</span></span>
<span data-ttu-id="1ac32-106">O cmdlet **Get-AzureRmVMDiskEncryptionStatus** Obtém o status de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1ac32-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="1ac32-107">Ele exibe o status de criptografia do sistema operacional e dos volumes de dados.</span><span class="sxs-lookup"><span data-stu-id="1ac32-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="1ac32-108">Além do status de criptografia, ele também exibe a URL de segredo de criptografia, a URL da chave de criptografia de chave, as IDs de recurso dos **cofres** de chaves onde a chave de criptografia e a chave de criptografia de chave do volume do sistema operacional estão presentes.</span><span class="sxs-lookup"><span data-stu-id="1ac32-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="1ac32-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ac32-109">EXAMPLES</span></span>

### <span data-ttu-id="1ac32-110">Exemplo 1: obter o status de criptografia de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="1ac32-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="1ac32-111">Esse comando obtém o status de criptografia da máquina virtual chamada VM001.</span><span class="sxs-lookup"><span data-stu-id="1ac32-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="1ac32-112">OS</span><span class="sxs-lookup"><span data-stu-id="1ac32-112">PARAMETERS</span></span>

### <span data-ttu-id="1ac32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac32-113">-DefaultProfile</span></span>
<span data-ttu-id="1ac32-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac32-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ac32-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ac32-115">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac32-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ac32-116">-ResourceGroupName</span></span>
<span data-ttu-id="1ac32-117">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1ac32-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1ac32-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="1ac32-118">-VMName</span></span>
<span data-ttu-id="1ac32-119">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1ac32-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="1ac32-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac32-120">CommonParameters</span></span>
<span data-ttu-id="1ac32-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ac32-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac32-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ac32-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac32-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ac32-123">INPUTS</span></span>

## <span data-ttu-id="1ac32-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ac32-124">OUTPUTS</span></span>

## <span data-ttu-id="1ac32-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ac32-125">NOTES</span></span>

## <span data-ttu-id="1ac32-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ac32-126">RELATED LINKS</span></span>

[<span data-ttu-id="1ac32-127">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1ac32-127">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="1ac32-128">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1ac32-128">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


