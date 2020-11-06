---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: 576c623b942ec496d2800c1ad5432f72eb6911bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595705"
---
# <span data-ttu-id="21a25-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="21a25-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="21a25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21a25-102">SYNOPSIS</span></span>
<span data-ttu-id="21a25-103">Faz backup de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="21a25-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="21a25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21a25-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21a25-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21a25-105">DESCRIPTION</span></span>
<span data-ttu-id="21a25-106">O cmdlet **backup-AzApiManagement** faz a cópia de um serviço de gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="21a25-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="21a25-107">Esse cmdlet armazena o backup como um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="21a25-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="21a25-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21a25-108">EXAMPLES</span></span>

### <span data-ttu-id="21a25-109">Exemplo 1: fazer backup de um serviço de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="21a25-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="21a25-110">Esse comando faz backup de um serviço de gerenciamento de API em um blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="21a25-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="21a25-111">OS</span><span class="sxs-lookup"><span data-stu-id="21a25-111">PARAMETERS</span></span>

### <span data-ttu-id="21a25-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a25-112">-DefaultProfile</span></span>
<span data-ttu-id="21a25-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21a25-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21a25-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="21a25-114">-Name</span></span>
<span data-ttu-id="21a25-115">Especifica o nome da implantação de gerenciamento de API que este cmdlet faz backup.</span><span class="sxs-lookup"><span data-stu-id="21a25-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="21a25-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21a25-116">-PassThru</span></span>
<span data-ttu-id="21a25-117">Indica que esse cmdlet retorna o objeto **PsApiManagement** em backup, se a operação for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="21a25-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="21a25-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21a25-118">-ResourceGroupName</span></span>
<span data-ttu-id="21a25-119">Especifica o nome do grupo de recursos sob o qual existe a implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="21a25-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="21a25-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="21a25-120">-StorageContext</span></span>
<span data-ttu-id="21a25-121">Especifica um contexto de conexão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="21a25-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="21a25-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="21a25-122">-TargetBlobName</span></span>
<span data-ttu-id="21a25-123">Especifica o nome do blob para o backup.</span><span class="sxs-lookup"><span data-stu-id="21a25-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="21a25-124">Se o BLOB não existir, esse cmdlet o criará.</span><span class="sxs-lookup"><span data-stu-id="21a25-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="21a25-125">Esse cmdlet gera um valor padrão com base no seguinte padrão: {Name}-{YYYY-MM-DD-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="21a25-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="21a25-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="21a25-126">-TargetContainerName</span></span>
<span data-ttu-id="21a25-127">Especifica o nome do contêiner do blob para o backup.</span><span class="sxs-lookup"><span data-stu-id="21a25-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="21a25-128">Se o contêiner não existir, esse cmdlet o criará.</span><span class="sxs-lookup"><span data-stu-id="21a25-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="21a25-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a25-129">CommonParameters</span></span>
<span data-ttu-id="21a25-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21a25-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a25-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21a25-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a25-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21a25-132">INPUTS</span></span>

### <span data-ttu-id="21a25-133">System. String</span><span class="sxs-lookup"><span data-stu-id="21a25-133">System.String</span></span>

### <span data-ttu-id="21a25-134">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="21a25-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="21a25-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21a25-135">OUTPUTS</span></span>

### <span data-ttu-id="21a25-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="21a25-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="21a25-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21a25-137">NOTES</span></span>

## <span data-ttu-id="21a25-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21a25-138">RELATED LINKS</span></span>

[<span data-ttu-id="21a25-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="21a25-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="21a25-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="21a25-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="21a25-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="21a25-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="21a25-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="21a25-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


