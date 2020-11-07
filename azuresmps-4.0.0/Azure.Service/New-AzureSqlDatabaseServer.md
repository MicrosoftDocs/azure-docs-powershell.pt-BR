---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A0C674FC-A1D8-4068-8CAB-2EE0AECB8E68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 069b96809c0659028135e8c9a28e7e3c0ab8b3ae
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945971"
---
# <span data-ttu-id="d9926-101">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="d9926-101">New-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="d9926-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9926-102">SYNOPSIS</span></span>
<span data-ttu-id="d9926-103">Cria um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9926-103">Creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="d9926-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9926-104">SYNTAX</span></span>

```
New-AzureSqlDatabaseServer -AdministratorLogin <String> -AdministratorLoginPassword <String> -Location <String>
 [-Version <Single>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9926-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9926-105">DESCRIPTION</span></span>
<span data-ttu-id="d9926-106">O cmdlet **New-AzureSqlDatabaseServer** cria uma instância do servidor de banco de dados SQL do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d9926-106">The **New-AzureSqlDatabaseServer** cmdlet creates an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="d9926-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9926-107">EXAMPLES</span></span>

### <span data-ttu-id="d9926-108">Exemplo 1: criar um servidor</span><span class="sxs-lookup"><span data-stu-id="d9926-108">Example 1: Create a server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword"
```

<span data-ttu-id="d9926-109">Esse comando cria uma versão 11 do servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9926-109">This command creates a version 11 Azure SQL Database server.</span></span>

### <span data-ttu-id="d9926-110">Exemplo 2: criar um servidor da versão 12</span><span class="sxs-lookup"><span data-stu-id="d9926-110">Example 2: Create a version 12 server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword" -Version "12.0"
```

<span data-ttu-id="d9926-111">Este comando cria um servidor da versão 12.</span><span class="sxs-lookup"><span data-stu-id="d9926-111">This command creates a version 12 server.</span></span>

## <span data-ttu-id="d9926-112">OS</span><span class="sxs-lookup"><span data-stu-id="d9926-112">PARAMETERS</span></span>

### <span data-ttu-id="d9926-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="d9926-113">-AdministratorLogin</span></span>
<span data-ttu-id="d9926-114">Especifica o nome da conta de administrador para o novo servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9926-114">Specifies the administrator account name for the new Azure SQL Database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9926-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="d9926-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="d9926-116">Especifica a senha da conta de administrador para o servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9926-116">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="d9926-117">Você deve especificar uma senha forte.</span><span class="sxs-lookup"><span data-stu-id="d9926-117">You must specify a strong password.</span></span>
<span data-ttu-id="d9926-118">Para obter mais informações, consulte [senhas de alta segurança](https://go.microsoft.com/fwlink/p/?LinkId=154152) ( https://go.microsoft.com/fwlink/p/?LinkId=154152) na Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="d9926-118">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9926-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d9926-119">-Force</span></span>
<span data-ttu-id="d9926-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d9926-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9926-121">-Local</span><span class="sxs-lookup"><span data-stu-id="d9926-121">-Location</span></span>
<span data-ttu-id="d9926-122">Especifica o local do centro de dados onde esse cmdlet cria o servidor.</span><span class="sxs-lookup"><span data-stu-id="d9926-122">Specifies the location of the data center where this cmdlet creates the server.</span></span>
<span data-ttu-id="d9926-123">Para obter mais informações, consulte [regiões do Azure](https://azure.microsoft.com/regions/) ( https://azure.microsoft.com/regions/#services) na biblioteca do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9926-123">For more information, see [Azure Regions](https://azure.microsoft.com/regions/) (https://azure.microsoft.com/regions/#services) in the Azure library.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9926-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d9926-124">-Profile</span></span>
<span data-ttu-id="d9926-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d9926-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d9926-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d9926-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9926-127">-Versão</span><span class="sxs-lookup"><span data-stu-id="d9926-127">-Version</span></span>
<span data-ttu-id="d9926-128">Especifica a versão do novo servidor.</span><span class="sxs-lookup"><span data-stu-id="d9926-128">Specifies the version of the new server.</span></span>
<span data-ttu-id="d9926-129">Os valores válidos são: 2,0 e 12,0.</span><span class="sxs-lookup"><span data-stu-id="d9926-129">Valid values are: 2.0 and 12.0.</span></span>

```yaml
Type: Single
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9926-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d9926-130">-Confirm</span></span>
<span data-ttu-id="d9926-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9926-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9926-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9926-132">-WhatIf</span></span>
<span data-ttu-id="d9926-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9926-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9926-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9926-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9926-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9926-135">CommonParameters</span></span>
<span data-ttu-id="d9926-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9926-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9926-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9926-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9926-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9926-138">INPUTS</span></span>

## <span data-ttu-id="d9926-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9926-139">OUTPUTS</span></span>

### <span data-ttu-id="d9926-140">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="d9926-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="d9926-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9926-141">NOTES</span></span>

## <span data-ttu-id="d9926-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9926-142">RELATED LINKS</span></span>

[<span data-ttu-id="d9926-143">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="d9926-143">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="d9926-144">Criar servidor</span><span class="sxs-lookup"><span data-stu-id="d9926-144">Create Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505699.aspx)

[<span data-ttu-id="d9926-145">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="d9926-145">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="d9926-146">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="d9926-146">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="d9926-147">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="d9926-147">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="d9926-148">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="d9926-148">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


