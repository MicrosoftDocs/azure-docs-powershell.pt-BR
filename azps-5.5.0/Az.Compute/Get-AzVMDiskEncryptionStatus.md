---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 4ad5ef08f9c12693a2fa4b4b372ee1320f90fb76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116550"
---
# <span data-ttu-id="0ba4d-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="0ba4d-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="0ba4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ba4d-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba4d-103">Obtém o status de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="0ba4d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ba4d-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ba4d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ba4d-105">DESCRIPTION</span></span>
<span data-ttu-id="0ba4d-106">O cmdlet **Get-AzVMDiskEncryptionStatus** obtém o status de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="0ba4d-107">Ele exibe o status de criptografia do sistema operacional e dos volumes de dados.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="0ba4d-108">Além do status de criptografia, ele também exibe a URL secreta de criptografia, a URL da chave de criptografia, as IDs de recurso das **KeyVaults** onde a chave de criptografia e a chave de criptografia chave para volume do sistema operacional estão presentes.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="0ba4d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0ba4d-109">EXAMPLES</span></span>

### <span data-ttu-id="0ba4d-110">Exemplo 1: Obter o status de criptografia de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="0ba4d-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="0ba4d-111">Esse comando obtém o status de criptografia da máquina virtual chamada VM001.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="0ba4d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ba4d-112">PARAMETERS</span></span>

### <span data-ttu-id="0ba4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ba4d-113">-DefaultProfile</span></span>
<span data-ttu-id="0ba4d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ba4d-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="0ba4d-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="0ba4d-116">O nome do editor de extensão.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-116">The extension publisher name.</span></span> <span data-ttu-id="0ba4d-117">Especifique esse parâmetro apenas para substituir o valor padrão de "Microsoft.Azure.Security".</span><span class="sxs-lookup"><span data-stu-id="0ba4d-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="0ba4d-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="0ba4d-118">-ExtensionType</span></span>
<span data-ttu-id="0ba4d-119">O tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-119">The extension type.</span></span> <span data-ttu-id="0ba4d-120">Especifique este parâmetro para substituir seu valor padrão de "AzureDiskEncryption" para VMs do Windows e "AzureDiskEncryptionForLinux" para VMs do Linux.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="0ba4d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ba4d-121">-Name</span></span>
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

### <span data-ttu-id="0ba4d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ba4d-122">-ResourceGroupName</span></span>
<span data-ttu-id="0ba4d-123">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0ba4d-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="0ba4d-124">-VMName</span></span>
<span data-ttu-id="0ba4d-125">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="0ba4d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba4d-126">CommonParameters</span></span>
<span data-ttu-id="0ba4d-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba4d-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ba4d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba4d-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="0ba4d-129">INPUTS</span></span>

### <span data-ttu-id="0ba4d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0ba4d-130">System.String</span></span>

## <span data-ttu-id="0ba4d-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="0ba4d-131">OUTPUTS</span></span>

### <span data-ttu-id="0ba4d-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="0ba4d-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="0ba4d-133">Notas</span><span class="sxs-lookup"><span data-stu-id="0ba4d-133">NOTES</span></span>

## <span data-ttu-id="0ba4d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ba4d-134">RELATED LINKS</span></span>

[<span data-ttu-id="0ba4d-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0ba4d-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="0ba4d-136">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0ba4d-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


