---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: b208d7c0e0db028f1b3242a70be508fbbc3788ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609403"
---
# <span data-ttu-id="e2c29-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="e2c29-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="e2c29-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2c29-102">SYNOPSIS</span></span>
<span data-ttu-id="e2c29-103">Obtém o status de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e2c29-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2c29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2c29-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2c29-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2c29-105">DESCRIPTION</span></span>
<span data-ttu-id="e2c29-106">O cmdlet **Get-AzureRmVMDiskEncryptionStatus** Obtém o status de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e2c29-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="e2c29-107">Ele exibe o status de criptografia do sistema operacional e dos volumes de dados.</span><span class="sxs-lookup"><span data-stu-id="e2c29-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="e2c29-108">Além do status de criptografia, ele também exibe a URL de segredo de criptografia, a URL da chave de criptografia de chave, as IDs de recurso dos **cofres** de chaves onde a chave de criptografia e a chave de criptografia de chave do volume do sistema operacional estão presentes.</span><span class="sxs-lookup"><span data-stu-id="e2c29-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="e2c29-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2c29-109">EXAMPLES</span></span>

### <span data-ttu-id="e2c29-110">Exemplo 1: obter o status de criptografia de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="e2c29-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="e2c29-111">Esse comando obtém o status de criptografia da máquina virtual chamada VM001.</span><span class="sxs-lookup"><span data-stu-id="e2c29-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="e2c29-112">OS</span><span class="sxs-lookup"><span data-stu-id="e2c29-112">PARAMETERS</span></span>

### <span data-ttu-id="e2c29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2c29-113">-DefaultProfile</span></span>
<span data-ttu-id="e2c29-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2c29-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2c29-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="e2c29-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="e2c29-116">O nome do fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="e2c29-116">The extension publisher name.</span></span> <span data-ttu-id="e2c29-117">Especifique esse parâmetro somente para substituir o valor padrão de "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="e2c29-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2c29-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="e2c29-118">-ExtensionType</span></span>
<span data-ttu-id="e2c29-119">O tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="e2c29-119">The extension type.</span></span> <span data-ttu-id="e2c29-120">Especifique esse parâmetro para substituir o valor padrão de "AzureDiskEncryption" para VMs do Windows e "AzureDiskEncryptionForLinux" para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="e2c29-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2c29-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2c29-121">-Name</span></span>
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

### <span data-ttu-id="e2c29-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2c29-122">-ResourceGroupName</span></span>
<span data-ttu-id="e2c29-123">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e2c29-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e2c29-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="e2c29-124">-VMName</span></span>
<span data-ttu-id="e2c29-125">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e2c29-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="e2c29-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2c29-126">CommonParameters</span></span>
<span data-ttu-id="e2c29-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2c29-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2c29-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2c29-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2c29-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2c29-129">INPUTS</span></span>

### <span data-ttu-id="e2c29-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e2c29-130">System.String</span></span>

## <span data-ttu-id="e2c29-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2c29-131">OUTPUTS</span></span>

### <span data-ttu-id="e2c29-132">Microsoft. Azure. Commands. COMPUTE. Extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="e2c29-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="e2c29-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2c29-133">NOTES</span></span>

## <span data-ttu-id="e2c29-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2c29-134">RELATED LINKS</span></span>

[<span data-ttu-id="e2c29-135">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="e2c29-135">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="e2c29-136">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="e2c29-136">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


