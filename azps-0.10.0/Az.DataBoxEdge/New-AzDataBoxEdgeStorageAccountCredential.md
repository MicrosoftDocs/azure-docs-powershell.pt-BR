---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 399c4030f9cd3efd04ec41ce3ab3475f0a660f4f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776761"
---
# <span data-ttu-id="99d53-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="99d53-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="99d53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99d53-102">SYNOPSIS</span></span>
<span data-ttu-id="99d53-103">Cria novas credenciais para uma conta de armazenamento de borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99d53-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="99d53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99d53-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99d53-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99d53-105">DESCRIPTION</span></span>
<span data-ttu-id="99d53-106">O cmdlet **New-AzDataBoxEdgeStorageAccountCredential** cria uma nova credencial de conta de armazenamento de borda para um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="99d53-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="99d53-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99d53-107">EXAMPLES</span></span>

### <span data-ttu-id="99d53-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="99d53-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="99d53-109">OS</span><span class="sxs-lookup"><span data-stu-id="99d53-109">PARAMETERS</span></span>

### <span data-ttu-id="99d53-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99d53-110">-AsJob</span></span>
<span data-ttu-id="99d53-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="99d53-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99d53-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d53-112">-DefaultProfile</span></span>
<span data-ttu-id="99d53-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99d53-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99d53-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="99d53-114">-DeviceName</span></span>
<span data-ttu-id="99d53-115">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="99d53-115">Device Name</span></span>

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

### <span data-ttu-id="99d53-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="99d53-116">-EncryptionKey</span></span>
<span data-ttu-id="99d53-117">Chave de criptografia do dispositivo de borda</span><span class="sxs-lookup"><span data-stu-id="99d53-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="99d53-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="99d53-118">-Name</span></span>
<span data-ttu-id="99d53-119">Nome da conta de armazenamento a ser usada</span><span class="sxs-lookup"><span data-stu-id="99d53-119">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="99d53-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d53-120">-ResourceGroupName</span></span>
<span data-ttu-id="99d53-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="99d53-121">Resource Group Name</span></span>

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

### <span data-ttu-id="99d53-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="99d53-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="99d53-123">fornecer chave de acesso à conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="99d53-123">provide storage account access key</span></span>

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

### <span data-ttu-id="99d53-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="99d53-124">-StorageAccountType</span></span>
<span data-ttu-id="99d53-125">Possível tipo de acesso de armazenamento GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="99d53-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="99d53-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="99d53-126">-Confirm</span></span>
<span data-ttu-id="99d53-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99d53-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99d53-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99d53-128">-WhatIf</span></span>
<span data-ttu-id="99d53-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="99d53-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99d53-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="99d53-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99d53-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d53-131">CommonParameters</span></span>
<span data-ttu-id="99d53-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d53-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d53-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99d53-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d53-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99d53-134">INPUTS</span></span>

### <span data-ttu-id="99d53-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="99d53-135">None</span></span>

## <span data-ttu-id="99d53-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99d53-136">OUTPUTS</span></span>

### <span data-ttu-id="99d53-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="99d53-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="99d53-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99d53-138">NOTES</span></span>

## <span data-ttu-id="99d53-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99d53-139">RELATED LINKS</span></span>
