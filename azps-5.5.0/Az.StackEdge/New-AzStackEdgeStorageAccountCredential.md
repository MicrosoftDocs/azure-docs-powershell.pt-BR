---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: d4e9062b15e7d5ca7338e13cdcdf71506ba23e29
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113684"
---
# <span data-ttu-id="d2958-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d2958-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="d2958-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2958-102">SYNOPSIS</span></span>
<span data-ttu-id="d2958-103">Cria novas credenciais para uma conta de armazenamento de borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2958-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="d2958-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2958-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2958-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2958-105">DESCRIPTION</span></span>
<span data-ttu-id="d2958-106">O **cmdlet New-AzSt stackEdgeStorageAccountCredential** cria uma nova credencial de conta de armazenamento de borda para um dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="d2958-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="d2958-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d2958-107">EXAMPLES</span></span>

### <span data-ttu-id="d2958-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2958-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="d2958-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2958-109">PARAMETERS</span></span>

### <span data-ttu-id="d2958-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2958-110">-AsJob</span></span>
<span data-ttu-id="d2958-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d2958-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2958-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2958-112">-DefaultProfile</span></span>
<span data-ttu-id="d2958-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2958-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2958-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d2958-114">-DeviceName</span></span>
<span data-ttu-id="d2958-115">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="d2958-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2958-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d2958-116">-EncryptionKey</span></span>
<span data-ttu-id="d2958-117">Chave de criptografia do dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="d2958-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="d2958-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2958-118">-Name</span></span>
<span data-ttu-id="d2958-119">Nome da conta de armazenamento a ser usada</span><span class="sxs-lookup"><span data-stu-id="d2958-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2958-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2958-120">-ResourceGroupName</span></span>
<span data-ttu-id="d2958-121">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d2958-121">Resource Group Name</span></span>

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

### <span data-ttu-id="d2958-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="d2958-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="d2958-123">fornecer chave de acesso à conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d2958-123">provide storage account access key</span></span>

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

### <span data-ttu-id="d2958-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d2958-124">-StorageAccountType</span></span>
<span data-ttu-id="d2958-125">Possível tipo de Acesso de Armazenamento GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="d2958-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="d2958-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d2958-126">-Confirm</span></span>
<span data-ttu-id="d2958-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2958-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2958-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2958-128">-WhatIf</span></span>
<span data-ttu-id="d2958-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d2958-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2958-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2958-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2958-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2958-131">CommonParameters</span></span>
<span data-ttu-id="d2958-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2958-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2958-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2958-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2958-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="d2958-134">INPUTS</span></span>

### <span data-ttu-id="d2958-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d2958-135">None</span></span>

## <span data-ttu-id="d2958-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="d2958-136">OUTPUTS</span></span>

### <span data-ttu-id="d2958-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d2958-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="d2958-138">Notas</span><span class="sxs-lookup"><span data-stu-id="d2958-138">NOTES</span></span>

## <span data-ttu-id="d2958-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2958-139">RELATED LINKS</span></span>
