---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 9547a3f3aed86bd7458f9fbf1f1a4375e2d95086
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429929"
---
# <span data-ttu-id="f4b24-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f4b24-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="f4b24-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4b24-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b24-103">Define a credencial de conta de armazenamento para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4b24-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="f4b24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4b24-104">SYNTAX</span></span>

### <span data-ttu-id="f4b24-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f4b24-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4b24-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4b24-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4b24-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4b24-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4b24-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4b24-108">DESCRIPTION</span></span>
<span data-ttu-id="f4b24-109">O cmdlet **set-AzDataBoxEdgeStorageAccountCredential** atualiza a credencial da conta de armazenamento correspondente a uma conta de armazenamento no dispositivo de borda da caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="f4b24-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="f4b24-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4b24-110">EXAMPLES</span></span>

### <span data-ttu-id="f4b24-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f4b24-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="f4b24-112">Ajuda na rotação de teclas de acesso para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f4b24-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="f4b24-113">OS</span><span class="sxs-lookup"><span data-stu-id="f4b24-113">PARAMETERS</span></span>

### <span data-ttu-id="f4b24-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4b24-114">-AsJob</span></span>
<span data-ttu-id="f4b24-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f4b24-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4b24-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b24-116">-DefaultProfile</span></span>
<span data-ttu-id="f4b24-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b24-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4b24-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f4b24-118">-DeviceName</span></span>
<span data-ttu-id="f4b24-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="f4b24-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b24-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f4b24-120">-EncryptionKey</span></span>
<span data-ttu-id="f4b24-121">Chave de criptografia do dispositivo de borda</span><span class="sxs-lookup"><span data-stu-id="f4b24-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="f4b24-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4b24-122">-InputObject</span></span>
<span data-ttu-id="f4b24-123">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="f4b24-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b24-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4b24-124">-Name</span></span>
<span data-ttu-id="f4b24-125">Nome da conta de armazenamento a ser usada</span><span class="sxs-lookup"><span data-stu-id="f4b24-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b24-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4b24-126">-ResourceGroupName</span></span>
<span data-ttu-id="f4b24-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f4b24-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b24-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4b24-128">-ResourceId</span></span>
<span data-ttu-id="f4b24-129">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="f4b24-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b24-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="f4b24-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="f4b24-131">fornecer chave de acesso à conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f4b24-131">provide storage account access key</span></span>

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

### <span data-ttu-id="f4b24-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f4b24-132">-Confirm</span></span>
<span data-ttu-id="f4b24-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4b24-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4b24-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4b24-134">-WhatIf</span></span>
<span data-ttu-id="f4b24-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4b24-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4b24-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4b24-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4b24-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b24-137">CommonParameters</span></span>
<span data-ttu-id="f4b24-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4b24-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b24-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4b24-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b24-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4b24-140">INPUTS</span></span>

### <span data-ttu-id="f4b24-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f4b24-141">System.String</span></span>

### <span data-ttu-id="f4b24-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f4b24-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="f4b24-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4b24-143">OUTPUTS</span></span>

### <span data-ttu-id="f4b24-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f4b24-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="f4b24-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4b24-145">NOTES</span></span>

## <span data-ttu-id="f4b24-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4b24-146">RELATED LINKS</span></span>
