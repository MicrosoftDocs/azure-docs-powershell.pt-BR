---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 7d0a7537594bb41fbcc41a7ddf457820c9b29dd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889012"
---
# <span data-ttu-id="3e6dc-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="3e6dc-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="3e6dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e6dc-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6dc-103">Obtém o status de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3e6dc-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="3e6dc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3e6dc-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e6dc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3e6dc-105">DESCRIPTION</span></span>
<span data-ttu-id="3e6dc-106">O cmdlet **Get-AzVMDiskEncryptionStatus** obtém o status de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3e6dc-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="3e6dc-107">Ele exibe o status de criptografia do sistema operacional e dos volumes de dados.</span><span class="sxs-lookup"><span data-stu-id="3e6dc-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="3e6dc-108">Além do status de criptografia, ele também exibe a URL secreta de criptografia, a URL da chave de criptografia, as IDs de recurso dos **KeyVaults** onde a chave de criptografia e a chave de criptografia chave para o volume do sistema operacional estão presentes.</span><span class="sxs-lookup"><span data-stu-id="3e6dc-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="3e6dc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e6dc-109">EXAMPLES</span></span>

### <span data-ttu-id="3e6dc-110">Exemplo 1: Obter o status de criptografia de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="3e6dc-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="3e6dc-111">Este comando obtém o status de criptografia da máquina virtual chamada VM001.</span><span class="sxs-lookup"><span data-stu-id="3e6dc-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="3e6dc-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3e6dc-112">PARAMETERS</span></span>

### <span data-ttu-id="3e6dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6dc-113">-DefaultProfile</span></span>
<span data-ttu-id="3e6dc-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3e6dc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e6dc-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="3e6dc-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="3e6dc-116">O nome do editor de extensão.</span><span class="sxs-lookup"><span data-stu-id="3e6dc-116">The extension publisher name.</span></span> <span data-ttu-id="3e6dc-117">Especifique esse parâmetro apenas para substituir o valor padrão de "Microsoft.Azure.Security".</span><span class="sxs-lookup"><span data-stu-id="3e6dc-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="3e6dc-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="3e6dc-118">-ExtensionType</span></span>
<span data-ttu-id="3e6dc-119">O tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="3e6dc-119">The extension type.</span></span> <span data-ttu-id="3e6dc-120">Especifique esse parâmetro para substituir seu valor padrão de "AzureDiskEncryption" para VMs do Windows e "AzureDiskEncryptionForLinux" para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="3e6dc-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="3e6dc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3e6dc-121">-Name</span></span>
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

### <span data-ttu-id="3e6dc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e6dc-122">-ResourceGroupName</span></span>
<span data-ttu-id="3e6dc-123">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3e6dc-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3e6dc-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="3e6dc-124">-VMName</span></span>
<span data-ttu-id="3e6dc-125">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3e6dc-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="3e6dc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6dc-126">CommonParameters</span></span>
<span data-ttu-id="3e6dc-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e6dc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6dc-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e6dc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6dc-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e6dc-129">INPUTS</span></span>

### <span data-ttu-id="3e6dc-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3e6dc-130">System.String</span></span>

## <span data-ttu-id="3e6dc-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3e6dc-131">OUTPUTS</span></span>

### <span data-ttu-id="3e6dc-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="3e6dc-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="3e6dc-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="3e6dc-133">NOTES</span></span>

## <span data-ttu-id="3e6dc-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e6dc-134">RELATED LINKS</span></span>

[<span data-ttu-id="3e6dc-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="3e6dc-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="3e6dc-136">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="3e6dc-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


