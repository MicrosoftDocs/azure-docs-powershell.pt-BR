---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 89e727b836f28ac1972bcf15e872e2860a8a6672
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261038"
---
# <span data-ttu-id="9c087-101">Set-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="9c087-101">Set-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="9c087-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c087-102">SYNOPSIS</span></span>
<span data-ttu-id="9c087-103">Define a credencial de conta de armazenamento para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c087-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="9c087-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c087-104">SYNTAX</span></span>

### <span data-ttu-id="9c087-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9c087-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c087-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c087-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c087-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c087-107">SetByParentObjectParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c087-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c087-108">DESCRIPTION</span></span>
<span data-ttu-id="9c087-109">O cmdlet **set-AzStackEdgeStorageAccountCredential** atualiza a credencial da conta de armazenamento correspondente a uma conta de armazenamento no dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="9c087-109">The **Set-AzStackEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Stack Edge device.</span></span>

## <span data-ttu-id="9c087-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c087-110">EXAMPLES</span></span>

### <span data-ttu-id="9c087-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c087-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="9c087-112">Ajuda na rotação de teclas de acesso para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9c087-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="9c087-113">OS</span><span class="sxs-lookup"><span data-stu-id="9c087-113">PARAMETERS</span></span>

### <span data-ttu-id="9c087-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c087-114">-AsJob</span></span>
<span data-ttu-id="9c087-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9c087-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c087-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c087-116">-DefaultProfile</span></span>
<span data-ttu-id="9c087-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c087-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c087-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9c087-118">-DeviceName</span></span>
<span data-ttu-id="9c087-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="9c087-119">Device Name</span></span>

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

### <span data-ttu-id="9c087-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9c087-120">-EncryptionKey</span></span>
<span data-ttu-id="9c087-121">Chave de criptografia do dispositivo de borda</span><span class="sxs-lookup"><span data-stu-id="9c087-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="9c087-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c087-122">-InputObject</span></span>
<span data-ttu-id="9c087-123">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="9c087-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c087-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c087-124">-Name</span></span>
<span data-ttu-id="9c087-125">Nome da conta de armazenamento a ser usada</span><span class="sxs-lookup"><span data-stu-id="9c087-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c087-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c087-126">-ResourceGroupName</span></span>
<span data-ttu-id="9c087-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9c087-127">Resource Group Name</span></span>

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

### <span data-ttu-id="9c087-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c087-128">-ResourceId</span></span>
<span data-ttu-id="9c087-129">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="9c087-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="9c087-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="9c087-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="9c087-131">fornecer chave de acesso à conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9c087-131">provide storage account access key</span></span>

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

### <span data-ttu-id="9c087-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9c087-132">-Confirm</span></span>
<span data-ttu-id="9c087-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c087-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c087-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c087-134">-WhatIf</span></span>
<span data-ttu-id="9c087-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c087-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c087-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c087-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c087-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c087-137">CommonParameters</span></span>
<span data-ttu-id="9c087-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c087-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c087-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c087-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c087-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c087-140">INPUTS</span></span>

### <span data-ttu-id="9c087-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9c087-141">System.String</span></span>

### <span data-ttu-id="9c087-142">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="9c087-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="9c087-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c087-143">OUTPUTS</span></span>

### <span data-ttu-id="9c087-144">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="9c087-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="9c087-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c087-145">NOTES</span></span>

## <span data-ttu-id="9c087-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c087-146">RELATED LINKS</span></span>
