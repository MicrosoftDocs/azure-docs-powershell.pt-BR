---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/backup-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: d8f243b0b02d724a3979b8c8f318be8e58623cf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432829"
---
# <span data-ttu-id="bfe36-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="bfe36-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="bfe36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfe36-102">SYNOPSIS</span></span>
<span data-ttu-id="bfe36-103">Faz backup de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="bfe36-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfe36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfe36-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfe36-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfe36-105">DESCRIPTION</span></span>
<span data-ttu-id="bfe36-106">O cmdlet **backup-AzureRmApiManagement** faz a cópia de um serviço de gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfe36-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="bfe36-107">Esse cmdlet armazena o backup como um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfe36-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="bfe36-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfe36-108">EXAMPLES</span></span>

### <span data-ttu-id="bfe36-109">Exemplo 1: fazer backup de um serviço de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="bfe36-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="bfe36-110">Esse comando faz backup de um serviço de gerenciamento de API em um blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bfe36-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="bfe36-111">OS</span><span class="sxs-lookup"><span data-stu-id="bfe36-111">PARAMETERS</span></span>

### <span data-ttu-id="bfe36-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfe36-112">-DefaultProfile</span></span>
<span data-ttu-id="bfe36-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfe36-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfe36-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfe36-114">-Name</span></span>
<span data-ttu-id="bfe36-115">Especifica o nome da implantação de gerenciamento de API que este cmdlet faz backup.</span><span class="sxs-lookup"><span data-stu-id="bfe36-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="bfe36-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfe36-116">-PassThru</span></span>
<span data-ttu-id="bfe36-117">Indica que esse cmdlet retorna o objeto **PsApiManagement** em backup, se a operação for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bfe36-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="bfe36-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfe36-118">-ResourceGroupName</span></span>
<span data-ttu-id="bfe36-119">Especifica o nome do grupo de recursos sob o qual existe a implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="bfe36-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="bfe36-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="bfe36-120">-StorageContext</span></span>
<span data-ttu-id="bfe36-121">Especifica um contexto de conexão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bfe36-121">Specifies a storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe36-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="bfe36-122">-TargetBlobName</span></span>
<span data-ttu-id="bfe36-123">Especifica o nome do blob para o backup.</span><span class="sxs-lookup"><span data-stu-id="bfe36-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="bfe36-124">Se o BLOB não existir, esse cmdlet o criará.</span><span class="sxs-lookup"><span data-stu-id="bfe36-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="bfe36-125">Esse cmdlet gera um valor padrão com base no seguinte padrão: {Name}-{YYYY-MM-DD-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="bfe36-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfe36-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="bfe36-126">-TargetContainerName</span></span>
<span data-ttu-id="bfe36-127">Especifica o nome do contêiner do blob para o backup.</span><span class="sxs-lookup"><span data-stu-id="bfe36-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="bfe36-128">Se o contêiner não existir, esse cmdlet o criará.</span><span class="sxs-lookup"><span data-stu-id="bfe36-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="bfe36-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfe36-129">CommonParameters</span></span>
<span data-ttu-id="bfe36-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfe36-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfe36-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfe36-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfe36-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfe36-132">INPUTS</span></span>

### <span data-ttu-id="bfe36-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bfe36-133">System.String</span></span>

### <span data-ttu-id="bfe36-134">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bfe36-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bfe36-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfe36-135">OUTPUTS</span></span>

### <span data-ttu-id="bfe36-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="bfe36-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="bfe36-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfe36-137">NOTES</span></span>

## <span data-ttu-id="bfe36-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfe36-138">RELATED LINKS</span></span>

[<span data-ttu-id="bfe36-139">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="bfe36-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="bfe36-140">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="bfe36-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="bfe36-141">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="bfe36-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="bfe36-142">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="bfe36-142">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


