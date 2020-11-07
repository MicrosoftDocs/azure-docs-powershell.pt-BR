---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiskencryptionstatus
schema: 2.0.0
ms.openlocfilehash: 667ebae58974b2dc68d19daa6a4f3a9d2e98075d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785273"
---
# <span data-ttu-id="55093-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="55093-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="55093-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55093-102">SYNOPSIS</span></span>
<span data-ttu-id="55093-103">Obtém o status de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="55093-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55093-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55093-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55093-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55093-105">DESCRIPTION</span></span>
<span data-ttu-id="55093-106">O cmdlet **Get-AzureRmVMDiskEncryptionStatus** Obtém o status de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="55093-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="55093-107">Ele exibe o status de criptografia do sistema operacional e dos volumes de dados.</span><span class="sxs-lookup"><span data-stu-id="55093-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="55093-108">Além do status de criptografia, ele também exibe a URL de segredo de criptografia, a URL da chave de criptografia de chave, as IDs de recurso dos **cofres** de chaves onde a chave de criptografia e a chave de criptografia de chave do volume do sistema operacional estão presentes.</span><span class="sxs-lookup"><span data-stu-id="55093-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="55093-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55093-109">EXAMPLES</span></span>

### <span data-ttu-id="55093-110">Exemplo 1: obter o status de criptografia de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="55093-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="55093-111">Esse comando obtém o status de criptografia da máquina virtual chamada VM001.</span><span class="sxs-lookup"><span data-stu-id="55093-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="55093-112">OS</span><span class="sxs-lookup"><span data-stu-id="55093-112">PARAMETERS</span></span>

### <span data-ttu-id="55093-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55093-113">-DefaultProfile</span></span>
<span data-ttu-id="55093-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55093-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55093-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="55093-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="55093-116">O nome do fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="55093-116">The extension publisher name.</span></span> <span data-ttu-id="55093-117">Especifique esse parâmetro somente para substituir o valor padrão de "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="55093-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55093-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="55093-118">-ExtensionType</span></span>
<span data-ttu-id="55093-119">O tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="55093-119">The extension type.</span></span> <span data-ttu-id="55093-120">Especifique esse parâmetro para substituir o valor padrão de "AzureDiskEncryption" para VMs do Windows e "AzureDiskEncryptionForLinux" para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="55093-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55093-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="55093-121">-Name</span></span>
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

### <span data-ttu-id="55093-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55093-122">-ResourceGroupName</span></span>
<span data-ttu-id="55093-123">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="55093-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="55093-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="55093-124">-VMName</span></span>
<span data-ttu-id="55093-125">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="55093-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="55093-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55093-126">CommonParameters</span></span>
<span data-ttu-id="55093-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55093-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55093-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55093-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55093-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55093-129">INPUTS</span></span>

### <span data-ttu-id="55093-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="55093-130">None</span></span>
<span data-ttu-id="55093-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="55093-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55093-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55093-132">OUTPUTS</span></span>

### <span data-ttu-id="55093-133">Microsoft. Azure. Commands. COMPUTE. Extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="55093-133">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="55093-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55093-134">NOTES</span></span>

## <span data-ttu-id="55093-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55093-135">RELATED LINKS</span></span>

[<span data-ttu-id="55093-136">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="55093-136">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="55093-137">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="55093-137">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


