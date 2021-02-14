---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 54d74b40230f67a31e023ef4933d3480bc5c2b42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115871"
---
# <span data-ttu-id="0d7a3-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0d7a3-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="0d7a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d7a3-102">SYNOPSIS</span></span>
<span data-ttu-id="0d7a3-103">Cria novas credenciais para uma conta de armazenamento de borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="0d7a3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d7a3-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d7a3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d7a3-105">DESCRIPTION</span></span>
<span data-ttu-id="0d7a3-106">O **cmdlet New-AzDataBoxEdgeStorageAccountCredential** cria uma nova credencial de conta de armazenamento de borda para um dispositivo de Borda de Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="0d7a3-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0d7a3-107">EXAMPLES</span></span>

### <span data-ttu-id="0d7a3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0d7a3-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="0d7a3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d7a3-109">PARAMETERS</span></span>

### <span data-ttu-id="0d7a3-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d7a3-110">-AsJob</span></span>
<span data-ttu-id="0d7a3-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0d7a3-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d7a3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d7a3-112">-DefaultProfile</span></span>
<span data-ttu-id="0d7a3-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d7a3-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0d7a3-114">-DeviceName</span></span>
<span data-ttu-id="0d7a3-115">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="0d7a3-115">Device Name</span></span>

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

### <span data-ttu-id="0d7a3-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0d7a3-116">-EncryptionKey</span></span>
<span data-ttu-id="0d7a3-117">Chave de criptografia do dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="0d7a3-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="0d7a3-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d7a3-118">-Name</span></span>
<span data-ttu-id="0d7a3-119">Nome da conta de armazenamento a ser usada</span><span class="sxs-lookup"><span data-stu-id="0d7a3-119">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="0d7a3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d7a3-120">-ResourceGroupName</span></span>
<span data-ttu-id="0d7a3-121">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="0d7a3-121">Resource Group Name</span></span>

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

### <span data-ttu-id="0d7a3-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="0d7a3-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="0d7a3-123">fornecer chave de acesso à conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0d7a3-123">provide storage account access key</span></span>

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

### <span data-ttu-id="0d7a3-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0d7a3-124">-StorageAccountType</span></span>
<span data-ttu-id="0d7a3-125">Possível tipo de Acesso de Armazenamento GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="0d7a3-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="0d7a3-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0d7a3-126">-Confirm</span></span>
<span data-ttu-id="0d7a3-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d7a3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d7a3-128">-WhatIf</span></span>
<span data-ttu-id="0d7a3-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d7a3-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d7a3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d7a3-131">CommonParameters</span></span>
<span data-ttu-id="0d7a3-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d7a3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d7a3-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d7a3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d7a3-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="0d7a3-134">INPUTS</span></span>

### <span data-ttu-id="0d7a3-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0d7a3-135">None</span></span>

## <span data-ttu-id="0d7a3-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="0d7a3-136">OUTPUTS</span></span>

### <span data-ttu-id="0d7a3-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0d7a3-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="0d7a3-138">Notas</span><span class="sxs-lookup"><span data-stu-id="0d7a3-138">NOTES</span></span>

## <span data-ttu-id="0d7a3-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d7a3-139">RELATED LINKS</span></span>
