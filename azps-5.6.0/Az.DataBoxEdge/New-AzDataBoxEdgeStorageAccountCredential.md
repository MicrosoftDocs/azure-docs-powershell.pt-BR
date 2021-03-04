---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 23fe08b273b95cd5ad3866437d131f432e6cee38
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888709"
---
# <span data-ttu-id="8bcfc-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8bcfc-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="8bcfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bcfc-102">SYNOPSIS</span></span>
<span data-ttu-id="8bcfc-103">Cria novas credenciais para uma conta de armazenamento de borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8bcfc-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="8bcfc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8bcfc-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bcfc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8bcfc-105">DESCRIPTION</span></span>
<span data-ttu-id="8bcfc-106">O cmdlet **New-AzDataBoxEdgeStorageAccountCredential** cria uma nova credencial de conta de armazenamento de borda para um dispositivo de Borda de Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="8bcfc-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="8bcfc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bcfc-107">EXAMPLES</span></span>

### <span data-ttu-id="8bcfc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8bcfc-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="8bcfc-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8bcfc-109">PARAMETERS</span></span>

### <span data-ttu-id="8bcfc-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bcfc-110">-AsJob</span></span>
<span data-ttu-id="8bcfc-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8bcfc-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8bcfc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bcfc-112">-DefaultProfile</span></span>
<span data-ttu-id="8bcfc-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bcfc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bcfc-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8bcfc-114">-DeviceName</span></span>
<span data-ttu-id="8bcfc-115">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8bcfc-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcfc-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8bcfc-116">-EncryptionKey</span></span>
<span data-ttu-id="8bcfc-117">Chave de criptografia do dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="8bcfc-117">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcfc-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8bcfc-118">-Name</span></span>
<span data-ttu-id="8bcfc-119">Nome da conta de armazenamento a ser usada</span><span class="sxs-lookup"><span data-stu-id="8bcfc-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcfc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bcfc-120">-ResourceGroupName</span></span>
<span data-ttu-id="8bcfc-121">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8bcfc-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcfc-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="8bcfc-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="8bcfc-123">fornecer chave de acesso à conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8bcfc-123">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcfc-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="8bcfc-124">-StorageAccountType</span></span>
<span data-ttu-id="8bcfc-125">Possível tipo de Acesso de Armazenamento GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="8bcfc-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcfc-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bcfc-126">-Confirm</span></span>
<span data-ttu-id="8bcfc-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bcfc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bcfc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bcfc-128">-WhatIf</span></span>
<span data-ttu-id="8bcfc-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8bcfc-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8bcfc-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8bcfc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bcfc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bcfc-131">CommonParameters</span></span>
<span data-ttu-id="8bcfc-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bcfc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bcfc-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bcfc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bcfc-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8bcfc-134">INPUTS</span></span>

### <span data-ttu-id="8bcfc-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8bcfc-135">None</span></span>

## <span data-ttu-id="8bcfc-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8bcfc-136">OUTPUTS</span></span>

### <span data-ttu-id="8bcfc-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8bcfc-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="8bcfc-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="8bcfc-138">NOTES</span></span>

## <span data-ttu-id="8bcfc-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bcfc-139">RELATED LINKS</span></span>
