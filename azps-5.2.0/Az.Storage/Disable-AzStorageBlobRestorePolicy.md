---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 8e68400eeaedd6529ffc4069b36c6f73e25864f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261018"
---
# <span data-ttu-id="7bcaa-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="7bcaa-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="7bcaa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bcaa-102">SYNOPSIS</span></span>
<span data-ttu-id="7bcaa-103">Desabilita a política de restauração de BLOB em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7bcaa-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="7bcaa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bcaa-104">SYNTAX</span></span>

### <span data-ttu-id="7bcaa-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7bcaa-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bcaa-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="7bcaa-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bcaa-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="7bcaa-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bcaa-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7bcaa-108">DESCRIPTION</span></span>
<span data-ttu-id="7bcaa-109">O cmdlet **Disable-AzStorageBlobRestorePolicy** desabilita a política de restauração de BLOB para o serviço de blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7bcaa-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="7bcaa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bcaa-110">EXAMPLES</span></span>

### <span data-ttu-id="7bcaa-111">Exemplo 1: desabilita a política de restauração de BLOB para o serviço de blob de armazenamento do Azure em uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7bcaa-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="7bcaa-112">Este comando desabilita a política de restauração de BLOB para o serviço de blob de armazenamento do Azure em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7bcaa-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="7bcaa-113">OS</span><span class="sxs-lookup"><span data-stu-id="7bcaa-113">PARAMETERS</span></span>

### <span data-ttu-id="7bcaa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bcaa-114">-DefaultProfile</span></span>
<span data-ttu-id="7bcaa-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7bcaa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bcaa-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bcaa-116">-PassThru</span></span>
<span data-ttu-id="7bcaa-117">Display Serviceproperties</span><span class="sxs-lookup"><span data-stu-id="7bcaa-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="7bcaa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bcaa-118">-ResourceGroupName</span></span>
<span data-ttu-id="7bcaa-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7bcaa-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bcaa-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bcaa-120">-ResourceId</span></span>
<span data-ttu-id="7bcaa-121">Insira uma ID de recurso da conta de armazenamento ou uma ID do recurso de propriedades do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="7bcaa-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bcaa-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7bcaa-122">-StorageAccount</span></span>
<span data-ttu-id="7bcaa-123">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7bcaa-123">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bcaa-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7bcaa-124">-StorageAccountName</span></span>
<span data-ttu-id="7bcaa-125">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7bcaa-125">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bcaa-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7bcaa-126">-Confirm</span></span>
<span data-ttu-id="7bcaa-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bcaa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bcaa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bcaa-128">-WhatIf</span></span>
<span data-ttu-id="7bcaa-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7bcaa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bcaa-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7bcaa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bcaa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bcaa-131">CommonParameters</span></span>
<span data-ttu-id="7bcaa-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bcaa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bcaa-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bcaa-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bcaa-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7bcaa-134">INPUTS</span></span>

### <span data-ttu-id="7bcaa-135">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7bcaa-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="7bcaa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7bcaa-136">System.String</span></span>

## <span data-ttu-id="7bcaa-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7bcaa-137">OUTPUTS</span></span>

### <span data-ttu-id="7bcaa-138">Microsoft. Azure. Commands. Management. Storage. Models. PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="7bcaa-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="7bcaa-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7bcaa-139">NOTES</span></span>

## <span data-ttu-id="7bcaa-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bcaa-140">RELATED LINKS</span></span>
