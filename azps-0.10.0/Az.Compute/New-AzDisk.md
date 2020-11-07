---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDisk.md
ms.openlocfilehash: 1eea8504f974e7ffc504520a5b5abc036c4d3e2a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776977"
---
# <span data-ttu-id="1b179-101">New-AzDisk</span><span class="sxs-lookup"><span data-stu-id="1b179-101">New-AzDisk</span></span>

## <span data-ttu-id="1b179-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b179-102">SYNOPSIS</span></span>
<span data-ttu-id="1b179-103">Cria um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="1b179-103">Creates a managed disk.</span></span>

## <span data-ttu-id="1b179-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b179-104">SYNTAX</span></span>

```
New-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b179-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b179-105">DESCRIPTION</span></span>
<span data-ttu-id="1b179-106">O cmdlet **New-AzDisk** cria um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="1b179-106">The **New-AzDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="1b179-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b179-107">EXAMPLES</span></span>

### <span data-ttu-id="1b179-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1b179-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="1b179-109">O primeiro comando cria um objeto de disco vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1b179-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="1b179-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="1b179-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="1b179-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="1b179-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="1b179-112">O último comando pega o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1b179-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1b179-113">OS</span><span class="sxs-lookup"><span data-stu-id="1b179-113">PARAMETERS</span></span>

### <span data-ttu-id="1b179-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b179-114">-AsJob</span></span>
<span data-ttu-id="1b179-115">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="1b179-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b179-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b179-116">-DefaultProfile</span></span>
<span data-ttu-id="1b179-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b179-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b179-118">-Disco</span><span class="sxs-lookup"><span data-stu-id="1b179-118">-Disk</span></span>
<span data-ttu-id="1b179-119">Especifica um objeto de disco local.</span><span class="sxs-lookup"><span data-stu-id="1b179-119">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b179-120">-Diskname</span><span class="sxs-lookup"><span data-stu-id="1b179-120">-DiskName</span></span>
<span data-ttu-id="1b179-121">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="1b179-121">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b179-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b179-122">-ResourceGroupName</span></span>
<span data-ttu-id="1b179-123">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1b179-123">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b179-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1b179-124">-Confirm</span></span>
<span data-ttu-id="1b179-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b179-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b179-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b179-126">-WhatIf</span></span>
<span data-ttu-id="1b179-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1b179-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b179-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1b179-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b179-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b179-129">CommonParameters</span></span>
<span data-ttu-id="1b179-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b179-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b179-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b179-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b179-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b179-132">INPUTS</span></span>

### <span data-ttu-id="1b179-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1b179-133">System.String</span></span>
<span data-ttu-id="1b179-134">Microsoft. Azure. Management. COMPUTE. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="1b179-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="1b179-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b179-135">OUTPUTS</span></span>

### <span data-ttu-id="1b179-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="1b179-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="1b179-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b179-137">NOTES</span></span>

## <span data-ttu-id="1b179-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b179-138">RELATED LINKS</span></span>

