---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 22eac04b24e8fec1778578f4e54792b5dcde6d1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440870"
---
# <span data-ttu-id="3feff-101">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3feff-101">Set-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="3feff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3feff-102">SYNOPSIS</span></span>
<span data-ttu-id="3feff-103">Modifica uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3feff-103">Modifies a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3feff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3feff-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3feff-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3feff-105">DESCRIPTION</span></span>
<span data-ttu-id="3feff-106">O cmdlet **set-AzureRmDataLakeStoreAccount** modifica uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3feff-106">The **Set-AzureRmDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="3feff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3feff-107">EXAMPLES</span></span>

### <span data-ttu-id="3feff-108">Exemplo 1: adicionar uma marca a uma conta</span><span class="sxs-lookup"><span data-stu-id="3feff-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="3feff-109">Esse comando adiciona a marca especificada à conta data Lake Store chamada ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="3feff-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="3feff-110">OS</span><span class="sxs-lookup"><span data-stu-id="3feff-110">PARAMETERS</span></span>

### <span data-ttu-id="3feff-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="3feff-111">-AllowAzureIpState</span></span>
<span data-ttu-id="3feff-112">Opcionalmente, permitir/bloquear IPs de origem do Azure por meio do firewall.</span><span class="sxs-lookup"><span data-stu-id="3feff-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: FirewallAllowAzureIpsState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3feff-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="3feff-113">-DefaultGroup</span></span>
<span data-ttu-id="3feff-114">Especifica a ID de um grupo de diretórios do AzureActive.</span><span class="sxs-lookup"><span data-stu-id="3feff-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="3feff-115">Este grupo é o grupo padrão para arquivos e pastas que você criar.</span><span class="sxs-lookup"><span data-stu-id="3feff-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3feff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3feff-116">-DefaultProfile</span></span>
<span data-ttu-id="3feff-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3feff-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3feff-118">-Firewallstate</span><span class="sxs-lookup"><span data-stu-id="3feff-118">-FirewallState</span></span>
<span data-ttu-id="3feff-119">Opcionalmente, habilite ou desabilite as regras de firewall existentes.</span><span class="sxs-lookup"><span data-stu-id="3feff-119">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: FirewallState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3feff-120">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="3feff-120">-KeyVersion</span></span>
<span data-ttu-id="3feff-121">Se o tipo de criptografia for atribuído pelo usuário, o usuário poderá girar a respectiva versão da chave com esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3feff-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3feff-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3feff-122">-Name</span></span>
<span data-ttu-id="3feff-123">Especifica o nome de uma conta do repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="3feff-123">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="3feff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3feff-124">-ResourceGroupName</span></span>
<span data-ttu-id="3feff-125">Especifica o nome do grupo de recursos que contém a conta do data Lake Store a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="3feff-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

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

### <span data-ttu-id="3feff-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="3feff-126">-Tag</span></span>
<span data-ttu-id="3feff-127">Especifica marcas como pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="3feff-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="3feff-128">Você pode usar marcas para identificar uma conta do data Lake Store de outros recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3feff-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3feff-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="3feff-129">-Tier</span></span>
<span data-ttu-id="3feff-130">A camada de compromisso desejada para esta conta usar.</span><span class="sxs-lookup"><span data-stu-id="3feff-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3feff-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="3feff-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="3feff-132">Opcionalmente, habilite ou desabilite os provedores de ID confiáveis existentes.</span><span class="sxs-lookup"><span data-stu-id="3feff-132">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: TrustedIdProviderState
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3feff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3feff-133">CommonParameters</span></span>
<span data-ttu-id="3feff-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3feff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3feff-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3feff-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3feff-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3feff-136">INPUTS</span></span>

### <span data-ttu-id="3feff-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3feff-137">None</span></span>
<span data-ttu-id="3feff-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3feff-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3feff-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3feff-139">OUTPUTS</span></span>

### <span data-ttu-id="3feff-140">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3feff-140">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="3feff-141">Os detalhes da conta atualizados.</span><span class="sxs-lookup"><span data-stu-id="3feff-141">The updated account details.</span></span>

## <span data-ttu-id="3feff-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3feff-142">NOTES</span></span>

## <span data-ttu-id="3feff-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3feff-143">RELATED LINKS</span></span>

[<span data-ttu-id="3feff-144">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3feff-144">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="3feff-145">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3feff-145">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="3feff-146">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3feff-146">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="3feff-147">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3feff-147">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


