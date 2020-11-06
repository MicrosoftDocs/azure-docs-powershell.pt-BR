---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/restore-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 3de18d5d7cc1c3525f1526beb5dd7337175eb041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611065"
---
# <span data-ttu-id="fcc6a-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="fcc6a-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="fcc6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fcc6a-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc6a-103">Restaura um serviço de gerenciamento de API do blob de armazenamento do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcc6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcc6a-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fcc6a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fcc6a-105">DESCRIPTION</span></span>
<span data-ttu-id="fcc6a-106">O cmdlet **Restore-AzureRmApiManagement** restaura um serviço de gerenciamento de API do backup especificado que reside em um blob AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="fcc6a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcc6a-107">EXAMPLES</span></span>

### <span data-ttu-id="fcc6a-108">Exemplo 1: restaurar um serviço de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="fcc6a-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="fcc6a-109">Esse comando restaura um serviço de gerenciamento de API do blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="fcc6a-110">OS</span><span class="sxs-lookup"><span data-stu-id="fcc6a-110">PARAMETERS</span></span>

### <span data-ttu-id="fcc6a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc6a-111">-DefaultProfile</span></span>
<span data-ttu-id="fcc6a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="fcc6a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fcc6a-113">-Name</span></span>
<span data-ttu-id="fcc6a-114">Especifica o nome da instância de gerenciamento de API que será restaurada com o backup.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcc6a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcc6a-115">-PassThru</span></span>
<span data-ttu-id="fcc6a-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fcc6a-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fcc6a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcc6a-118">-ResourceGroupName</span></span>
<span data-ttu-id="fcc6a-119">Especifica o nome do grupo de recursos sob o qual existe gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-119">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcc6a-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="fcc6a-120">-SourceBlobName</span></span>
<span data-ttu-id="fcc6a-121">Especifica o nome do blob de fonte de backup do armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-121">Specifies the name of the Azure storage backup source blob.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcc6a-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="fcc6a-122">-SourceContainerName</span></span>
<span data-ttu-id="fcc6a-123">Especifica o nome do contêiner da fonte de backup do armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-123">Specifies the name of the Azure storage backup source container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcc6a-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="fcc6a-124">-StorageContext</span></span>
<span data-ttu-id="fcc6a-125">Especifica o contexto de conexão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-125">Specifies the storage connection context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcc6a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc6a-126">CommonParameters</span></span>
<span data-ttu-id="fcc6a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc6a-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcc6a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc6a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fcc6a-129">INPUTS</span></span>

### <span data-ttu-id="fcc6a-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fcc6a-130">None</span></span>
<span data-ttu-id="fcc6a-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="fcc6a-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fcc6a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fcc6a-132">OUTPUTS</span></span>

### <span data-ttu-id="fcc6a-133">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="fcc6a-133">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="fcc6a-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fcc6a-134">NOTES</span></span>

## <span data-ttu-id="fcc6a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcc6a-135">RELATED LINKS</span></span>

[<span data-ttu-id="fcc6a-136">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="fcc6a-136">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="fcc6a-137">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="fcc6a-137">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="fcc6a-138">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="fcc6a-138">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="fcc6a-139">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="fcc6a-139">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)


