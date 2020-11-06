---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 9e19d8e205010ce55886761d2cbb7fd904d5277d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602076"
---
# <span data-ttu-id="42619-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="42619-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="42619-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42619-102">SYNOPSIS</span></span>
<span data-ttu-id="42619-103">Restaura um serviço de gerenciamento de API do blob de armazenamento do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="42619-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42619-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42619-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42619-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42619-105">DESCRIPTION</span></span>
<span data-ttu-id="42619-106">O cmdlet **Restore-AzureRmApiManagement** restaura um serviço de gerenciamento de API do backup especificado que reside em um blob AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="42619-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="42619-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42619-107">EXAMPLES</span></span>

### <span data-ttu-id="42619-108">Exemplo 1: restaurar um serviço de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="42619-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="42619-109">Esse comando restaura um serviço de gerenciamento de API do blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="42619-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="42619-110">OS</span><span class="sxs-lookup"><span data-stu-id="42619-110">PARAMETERS</span></span>

### <span data-ttu-id="42619-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="42619-111">-Name</span></span>
<span data-ttu-id="42619-112">Especifica o nome da instância de gerenciamento de API que será restaurada com o backup.</span><span class="sxs-lookup"><span data-stu-id="42619-112">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42619-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42619-113">-PassThru</span></span>
<span data-ttu-id="42619-114">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="42619-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="42619-115">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="42619-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="42619-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42619-116">-ResourceGroupName</span></span>
<span data-ttu-id="42619-117">Especifica o nome do grupo de recursos sob o qual existe gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="42619-117">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42619-118">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="42619-118">-SourceBlobName</span></span>
<span data-ttu-id="42619-119">Especifica o nome do blob de fonte de backup do armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="42619-119">Specifies the name of the Azure storage backup source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42619-120">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="42619-120">-SourceContainerName</span></span>
<span data-ttu-id="42619-121">Especifica o nome do contêiner da fonte de backup do armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="42619-121">Specifies the name of the Azure storage backup source container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42619-122">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="42619-122">-StorageContext</span></span>
<span data-ttu-id="42619-123">Especifica o contexto de conexão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="42619-123">Specifies the storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42619-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42619-124">-DefaultProfile</span></span>
<span data-ttu-id="42619-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42619-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42619-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42619-126">CommonParameters</span></span>
<span data-ttu-id="42619-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42619-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42619-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42619-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42619-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42619-129">INPUTS</span></span>

## <span data-ttu-id="42619-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42619-130">OUTPUTS</span></span>

### <span data-ttu-id="42619-131">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="42619-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="42619-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42619-132">NOTES</span></span>

## <span data-ttu-id="42619-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42619-133">RELATED LINKS</span></span>

[<span data-ttu-id="42619-134">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="42619-134">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="42619-135">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="42619-135">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="42619-136">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="42619-136">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="42619-137">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="42619-137">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)


