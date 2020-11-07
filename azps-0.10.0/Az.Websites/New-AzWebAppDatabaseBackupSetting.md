---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 7ea02fb05c64c751fc339c889098724b2822a8b8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776088"
---
# <span data-ttu-id="33dae-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="33dae-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="33dae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33dae-102">SYNOPSIS</span></span>

## <span data-ttu-id="33dae-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33dae-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33dae-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33dae-104">DESCRIPTION</span></span>
<span data-ttu-id="33dae-105">O cmdlet **New-AzWebAppDatabaseBackupSetting** cria uma nova configuração de backup do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="33dae-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="33dae-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33dae-106">EXAMPLES</span></span>

### <span data-ttu-id="33dae-107">1:</span><span class="sxs-lookup"><span data-stu-id="33dae-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="33dae-108">Cria uma configuração de backup de banco de dados (cadeia de conexão) do tipo sqlazure para o aplicativo especificado ContosoWebApp que está dentro do grupo de recursos-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="33dae-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="33dae-109">OS</span><span class="sxs-lookup"><span data-stu-id="33dae-109">PARAMETERS</span></span>

### <span data-ttu-id="33dae-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="33dae-110">-ConnectionString</span></span>
<span data-ttu-id="33dae-111">Cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="33dae-111">Connection String</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33dae-112">-ConnectionStringname</span><span class="sxs-lookup"><span data-stu-id="33dae-112">-ConnectionStringName</span></span>
<span data-ttu-id="33dae-113">Nome da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="33dae-113">Connection String Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33dae-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="33dae-114">-DatabaseType</span></span>
<span data-ttu-id="33dae-115">Tipo de banco de dados (por exemplo, "sqlazure" ou "MySql")</span><span class="sxs-lookup"><span data-stu-id="33dae-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33dae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33dae-116">-DefaultProfile</span></span>
<span data-ttu-id="33dae-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33dae-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33dae-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="33dae-118">-Name</span></span>
<span data-ttu-id="33dae-119">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="33dae-119">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33dae-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33dae-120">CommonParameters</span></span>
<span data-ttu-id="33dae-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33dae-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33dae-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33dae-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33dae-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33dae-123">INPUTS</span></span>

### <span data-ttu-id="33dae-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="33dae-124">None</span></span>
<span data-ttu-id="33dae-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="33dae-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33dae-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33dae-126">OUTPUTS</span></span>

### <span data-ttu-id="33dae-127">Microsoft. Azure. Management. WebSites. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="33dae-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="33dae-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33dae-128">NOTES</span></span>

## <span data-ttu-id="33dae-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33dae-129">RELATED LINKS</span></span>

