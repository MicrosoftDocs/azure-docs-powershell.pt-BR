---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 1b2a3855703c1d91a17cfd164f6a65ce218da486
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597441"
---
# <span data-ttu-id="0180b-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="0180b-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="0180b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0180b-102">SYNOPSIS</span></span>
<span data-ttu-id="0180b-103">Obtém o status de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0180b-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="0180b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0180b-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0180b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0180b-105">DESCRIPTION</span></span>
<span data-ttu-id="0180b-106">O cmdlet **Get-AzVMDiskEncryptionStatus** Obtém o status de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0180b-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="0180b-107">Ele exibe o status de criptografia do sistema operacional e dos volumes de dados.</span><span class="sxs-lookup"><span data-stu-id="0180b-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="0180b-108">Além do status de criptografia, ele também exibe a URL de segredo de criptografia, a URL da chave de criptografia de chave, as IDs de recurso dos **cofres** de chaves onde a chave de criptografia e a chave de criptografia de chave do volume do sistema operacional estão presentes.</span><span class="sxs-lookup"><span data-stu-id="0180b-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="0180b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0180b-109">EXAMPLES</span></span>

### <span data-ttu-id="0180b-110">Exemplo 1: obter o status de criptografia de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="0180b-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="0180b-111">Esse comando obtém o status de criptografia da máquina virtual chamada VM001.</span><span class="sxs-lookup"><span data-stu-id="0180b-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="0180b-112">OS</span><span class="sxs-lookup"><span data-stu-id="0180b-112">PARAMETERS</span></span>

### <span data-ttu-id="0180b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0180b-113">-DefaultProfile</span></span>
<span data-ttu-id="0180b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0180b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0180b-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="0180b-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="0180b-116">O nome do fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="0180b-116">The extension publisher name.</span></span> <span data-ttu-id="0180b-117">Especifique esse parâmetro somente para substituir o valor padrão de "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="0180b-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="0180b-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="0180b-118">-ExtensionType</span></span>
<span data-ttu-id="0180b-119">O tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="0180b-119">The extension type.</span></span> <span data-ttu-id="0180b-120">Especifique esse parâmetro para substituir o valor padrão de "AzureDiskEncryption" para VMs do Windows e "AzureDiskEncryptionForLinux" para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="0180b-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="0180b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0180b-121">-Name</span></span>
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

### <span data-ttu-id="0180b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0180b-122">-ResourceGroupName</span></span>
<span data-ttu-id="0180b-123">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0180b-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0180b-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="0180b-124">-VMName</span></span>
<span data-ttu-id="0180b-125">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0180b-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="0180b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0180b-126">CommonParameters</span></span>
<span data-ttu-id="0180b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0180b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0180b-128">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0180b-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0180b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0180b-129">INPUTS</span></span>

### <span data-ttu-id="0180b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0180b-130">System.String</span></span>

## <span data-ttu-id="0180b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0180b-131">OUTPUTS</span></span>

### <span data-ttu-id="0180b-132">Microsoft. Azure. Commands. COMPUTE. Extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="0180b-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="0180b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0180b-133">NOTES</span></span>

## <span data-ttu-id="0180b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0180b-134">RELATED LINKS</span></span>

[<span data-ttu-id="0180b-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0180b-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="0180b-136">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0180b-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


