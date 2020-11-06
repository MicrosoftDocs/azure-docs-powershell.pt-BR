---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 279216ad20783017f091143a7c440873c8e04946
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429289"
---
# <span data-ttu-id="1aca4-101">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="1aca4-101">Start-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="1aca4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1aca4-102">SYNOPSIS</span></span>
<span data-ttu-id="1aca4-103">Inicia a atualização de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="1aca4-103">Starts the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1aca4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1aca4-104">SYNTAX</span></span>

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1aca4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1aca4-105">DESCRIPTION</span></span>
<span data-ttu-id="1aca4-106">O cmdlet **Start-AzureRmSqlServerUpgrade** inicia a atualização de um servidor de banco de dados SQL do Azure versão 11 para a versão 12.</span><span class="sxs-lookup"><span data-stu-id="1aca4-106">The **Start-AzureRmSqlServerUpgrade** cmdlet starts the upgrade of an Azure SQL Database server version 11 to version 12.</span></span>
<span data-ttu-id="1aca4-107">Você pode monitorar o andamento de uma atualização usando o cmdlet Get-AzureRmSqlServerUpgrade.</span><span class="sxs-lookup"><span data-stu-id="1aca4-107">You can monitor the progress of an upgrade by using the Get-AzureRmSqlServerUpgrade cmdlet.</span></span>

## <span data-ttu-id="1aca4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1aca4-108">EXAMPLES</span></span>

### <span data-ttu-id="1aca4-109">Exemplo 1: atualizar um servidor</span><span class="sxs-lookup"><span data-stu-id="1aca4-109">Example 1: Upgrade a server</span></span>
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

<span data-ttu-id="1aca4-110">Esse comando atualiza o servidor chamado Server01 atribuído à TesourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1aca4-110">This command upgrades the server named server01 assigned to resource group TesourceGroup01.</span></span>

### <span data-ttu-id="1aca4-111">Exemplo 2: atualizar um servidor usando o tempo de agendamento e a recomendação de banco de dados</span><span class="sxs-lookup"><span data-stu-id="1aca4-111">Example 2: Upgrade a server by using schedule time and database recommendation</span></span>
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

<span data-ttu-id="1aca4-112">O primeiro comando cria um tempo cinco minutos no futuro usando o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="1aca4-112">The first command creates a time five minutes in the future by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="1aca4-113">O comando armazena a data na variável $ScheduleTime.</span><span class="sxs-lookup"><span data-stu-id="1aca4-113">The command stores the date in the variable $ScheduleTime.</span></span>
<span data-ttu-id="1aca4-114">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="1aca4-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="1aca4-115">O segundo comando cria um objeto **RecommendedDatabaseProperties** e armazena esse objeto na variável $DatabaseMap.</span><span class="sxs-lookup"><span data-stu-id="1aca4-115">The second command creates a **RecommendedDatabaseProperties** object, and then stores that object in the variable $DatabaseMap.</span></span>
<span data-ttu-id="1aca4-116">Os próximos três comandos atribuem valores às propriedades do objeto armazenadas em $DatabaseMap.</span><span class="sxs-lookup"><span data-stu-id="1aca4-116">The next three commands assign values to properties of the object stored in $DatabaseMap.</span></span>
<span data-ttu-id="1aca4-117">O comando final atualiza o servidor existente chamado Server01 para a versão 12,0.</span><span class="sxs-lookup"><span data-stu-id="1aca4-117">The final command upgrades the existing server named Server01 to version 12.0.</span></span>
<span data-ttu-id="1aca4-118">O mais cedo para atualizar é cinco minutos após você executar o comando, conforme especificado pela variável $ScheduleTime.</span><span class="sxs-lookup"><span data-stu-id="1aca4-118">The earliest time to upgrade is five minutes after you run the command, as specified by the $ScheduleTime variable.</span></span>
<span data-ttu-id="1aca4-119">Após a atualização, o banco de dados ContosoDB será executando a edição padrão e terá o objetivo de nível de serviço S0.</span><span class="sxs-lookup"><span data-stu-id="1aca4-119">After the upgrade, the database contosodb will be running the Standard edition and have the Service Level Objective S0.</span></span>

## <span data-ttu-id="1aca4-120">OS</span><span class="sxs-lookup"><span data-stu-id="1aca4-120">PARAMETERS</span></span>

### <span data-ttu-id="1aca4-121">-DatabaseCollection</span><span class="sxs-lookup"><span data-stu-id="1aca4-121">-DatabaseCollection</span></span>
<span data-ttu-id="1aca4-122">Especifica uma matriz de objetos **RecommendedDatabaseProperties** que este cmdlet usa para a atualização do servidor.</span><span class="sxs-lookup"><span data-stu-id="1aca4-122">Specifies an array of **RecommendedDatabaseProperties** objects that this cmdlet uses for the server upgrade.</span></span>

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aca4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aca4-123">-DefaultProfile</span></span>
<span data-ttu-id="1aca4-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1aca4-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1aca4-125">-ElasticPoolCollection</span><span class="sxs-lookup"><span data-stu-id="1aca4-125">-ElasticPoolCollection</span></span>
<span data-ttu-id="1aca4-126">Especifica uma matriz de objetos **UpgradeRecommendedElasticPoolProperties** a serem usados para a atualização do servidor.</span><span class="sxs-lookup"><span data-stu-id="1aca4-126">Specifies an array of **UpgradeRecommendedElasticPoolProperties** objects to use for the server upgrade.</span></span>

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aca4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aca4-127">-ResourceGroupName</span></span>
<span data-ttu-id="1aca4-128">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="1aca4-128">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="1aca4-129">-ScheduleUpgradeAfterUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="1aca4-129">-ScheduleUpgradeAfterUtcDateTime</span></span>
<span data-ttu-id="1aca4-130">Especifica a primeira vez, como um objeto **DateTime** , para atualizar o servidor.</span><span class="sxs-lookup"><span data-stu-id="1aca4-130">Specifies the earliest time, as a **DateTime** object, to upgrade the server.</span></span>
<span data-ttu-id="1aca4-131">Especifique um valor no formato ISO8601, no tempo universal coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="1aca4-131">Specify a value in the ISO8601 format, in Coordinated Universal Time (UTC).</span></span>
<span data-ttu-id="1aca4-132">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="1aca4-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aca4-133">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="1aca4-133">-ServerName</span></span>
<span data-ttu-id="1aca4-134">Especifica o nome do servidor que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="1aca4-134">Specifies the name of the server that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="1aca4-135">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="1aca4-135">-ServerVersion</span></span>
<span data-ttu-id="1aca4-136">Especifica a versão para a qual esse cmdlet atualiza o servidor.</span><span class="sxs-lookup"><span data-stu-id="1aca4-136">Specifies the version to which this cmdlet upgrades the server.</span></span>
<span data-ttu-id="1aca4-137">O único valor válido é 12,0.</span><span class="sxs-lookup"><span data-stu-id="1aca4-137">The only valid value is 12.0.</span></span>

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

### <span data-ttu-id="1aca4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aca4-138">CommonParameters</span></span>
<span data-ttu-id="1aca4-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aca4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aca4-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aca4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aca4-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1aca4-141">INPUTS</span></span>

### <span data-ttu-id="1aca4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1aca4-142">System.String</span></span>

## <span data-ttu-id="1aca4-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1aca4-143">OUTPUTS</span></span>

### <span data-ttu-id="1aca4-144">Microsoft. Azure. Commands. Sql. ServerUpgrade. Model. AzureSqlServerUpgradeStartModel</span><span class="sxs-lookup"><span data-stu-id="1aca4-144">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeStartModel</span></span>

## <span data-ttu-id="1aca4-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1aca4-145">NOTES</span></span>

## <span data-ttu-id="1aca4-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1aca4-146">RELATED LINKS</span></span>

[<span data-ttu-id="1aca4-147">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="1aca4-147">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="1aca4-148">Parar-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="1aca4-148">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="1aca4-149">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="1aca4-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


