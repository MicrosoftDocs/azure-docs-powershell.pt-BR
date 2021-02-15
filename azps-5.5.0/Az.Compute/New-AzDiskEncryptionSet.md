---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112126"
---
# <span data-ttu-id="d241d-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d241d-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="d241d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d241d-102">SYNOPSIS</span></span>
<span data-ttu-id="d241d-103">Cria um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="d241d-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="d241d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d241d-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d241d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d241d-105">DESCRIPTION</span></span>
<span data-ttu-id="d241d-106">Cria um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="d241d-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="d241d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d241d-107">EXAMPLES</span></span>

### <span data-ttu-id="d241d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d241d-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="d241d-109">Cria conjunto de criptografia de disco usando a chave ativa determinada no cofre de teclas.</span><span class="sxs-lookup"><span data-stu-id="d241d-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="d241d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d241d-110">PARAMETERS</span></span>

### <span data-ttu-id="d241d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d241d-111">-AsJob</span></span>
<span data-ttu-id="d241d-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d241d-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d241d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d241d-113">-DefaultProfile</span></span>
<span data-ttu-id="d241d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d241d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d241d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d241d-115">-InputObject</span></span>
<span data-ttu-id="d241d-116">O objeto local do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="d241d-116">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: (All)
Aliases: DiskEncryptionSet

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d241d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d241d-117">-Name</span></span>
<span data-ttu-id="d241d-118">Nome do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="d241d-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d241d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d241d-119">-ResourceGroupName</span></span>
<span data-ttu-id="d241d-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d241d-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d241d-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d241d-121">-Confirm</span></span>
<span data-ttu-id="d241d-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d241d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d241d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d241d-123">-WhatIf</span></span>
<span data-ttu-id="d241d-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d241d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d241d-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d241d-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d241d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d241d-126">CommonParameters</span></span>
<span data-ttu-id="d241d-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d241d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d241d-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d241d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d241d-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="d241d-129">INPUTS</span></span>

### <span data-ttu-id="d241d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d241d-130">System.String</span></span>

### <span data-ttu-id="d241d-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d241d-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="d241d-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="d241d-132">OUTPUTS</span></span>

### <span data-ttu-id="d241d-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d241d-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="d241d-134">Notas</span><span class="sxs-lookup"><span data-stu-id="d241d-134">NOTES</span></span>

## <span data-ttu-id="d241d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d241d-135">RELATED LINKS</span></span>
